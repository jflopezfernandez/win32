---
Description: Add a top level object after the frame hierarchy.
ms.assetid: 43b3cdb3-c6f0-4028-bf86-43d643fba73d
title: ID3DXSaveUserData::AddTopLevelDataObjectsPost method
ms.technology: desktop
ms.prod: windows
ms.author: windowssdkdev
ms.topic: article
ms.date: 05/31/2018
---

# ID3DXSaveUserData::AddTopLevelDataObjectsPost method

Add a top level object after the frame hierarchy.

## Syntax


```C++
HRESULT AddTopLevelDataObjectsPost(
  [in] LPD3DXFILESAVEOBJECT pXofSave
);
```



## Parameters

<dl> <dt>

*pXofSave* \[in\]
</dt> <dd>

Type: **[**LPD3DXFILESAVEOBJECT**](id3dxfilesaveobject.md)**

Pointer to a .x file save object. Use this pointer to call [**IDirectXFileSaveObject::CreateDataObject**](idirectxfilesaveobject--createdataobject.md) to create the data object to be saved. Then call [**IDirectXFileSaveObject::SaveData**](idirectxfilesaveobject--savedata.md) to save the data.

</dd> </dl>

## Return value

Type: **[**HRESULT**](https://msdn.microsoft.com/windows/desktop/455d07e9-52c3-4efb-a9dc-2955cbfd38cc)**

The return values of this method are implemented by an application programmer. In general, if no error occurs, program the method to return D3D\_OK. Otherwise, program the method to return an appropriate error message from [D3DERR](d3derr.md) or [**D3DXERR**](https://msdn.microsoft.com/windows/desktop/2318278e-e1e1-4cd8-a5ce-5c99f3bc47ba), as this will cause [**D3DXLoadMeshHierarchyFromX**](d3dxloadmeshhierarchyfromx.md) to fail also, and return the error.

## Requirements



|                    |                                                                                        |
|--------------------|----------------------------------------------------------------------------------------|
| Header<br/>  | <dl> <dt>D3dx9anim.h</dt> </dl> |
| Library<br/> | <dl> <dt>D3dx9.lib</dt> </dl>   |



## See also

<dl> <dt>

[ID3DXSaveUserData](id3dxsaveuserdata.md)
</dt> </dl>

 

 



