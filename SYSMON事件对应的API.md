# SYSMON事件所对应的API

通俗的说，sysmon对这些API的操作有监控，会生成事件响应。作为公鸡队，在做主机对抗的过程中，需要明白自己使用的工具可能会触发哪些SYSMON事件。

**工具**  ----*调用*---->  **API**  ----*对应*---->  **SYSMON EVENT**  ----*触发*---->  **告警**

## API to EVENT
- 1-ProcessCreate
  - CreateProcess
  - CreateProcessAsUser
  - CreateProcessWithLogon
  - CreateProcessWithToken

- 2-Process Changed File Creation Time
  - SetFileTime

- 5-Process Terminated
  - ExitProcess

- 6-Driver Loaded
  - LoadLibrary

- 7-Image Loaded
  - LoadLibrary
  - ImageLoad

- 8-CreateRemoteThread
  -  CreateRemoteThread

- 9-RawAccessRead
  - NtCreateFile
  - CreateFile

- 10-Process Access 
  - OpenProcess
  - NtOpenProcess

- 11-File Create
  - CopyFile
  - CreateFile
  - MoveFile
  - NtCreateFile
  - NtWriteFile

- 12-RegistryEvent(Object create and delete)
  - RegCreateKey
  - RegCreateKeyTransacted
  - RegDeleteKey
  - RegDeleteKeyTransacted
  - RegDeleteTree
  - RegDeleteValue
  - ZwCreateKey
  - ZwDeleteKey

- 13-Registry Event(Value Set)
  - RegSetKeyValue
  - RegSetValue
  - ZwSetValueKey

- 14-RegistryEvent(Key and Value Rename)
  - NtRenameKey

- 15-FileCreateStreamHash
  - NtCreateFile

- 17-PipeEvnet(Pipe Created)
  - CreateNamedPipe
  - CreatePipe

- 18-PipeEvent(Pipe Connected)
  - ConnectNamedPipe

- 22-DNS Event(DNS Query)
  - DNSQuery
