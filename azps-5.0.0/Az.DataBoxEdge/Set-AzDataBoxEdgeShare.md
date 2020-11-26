---
external help file: Microsoft.Azure.PowerShell.Cmdlets.DataBoxEdge.dll-Help.xml
Module Name: Az.DataBoxEdge
online version: https://docs.microsoft.com/en-us/powershell/module/az.databoxedge/set-azdataboxedgeshare
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/DataBoxEdge/DataBoxEdge/help/Set-AzDataBoxEdgeShare.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/DataBoxEdge/DataBoxEdge/help/Set-AzDataBoxEdgeShare.md
ms.openlocfilehash: 8bef754d7d9020193e4694953222a6579341c9ed
ms.sourcegitcommit: b4a38bcb0501a9016a4998efd377aa75d3ef9ce8
ms.translationtype: MT
ms.contentlocale: sv-SE
ms.lasthandoff: 10/27/2020
ms.locfileid: "94321107"
---
# <span data-ttu-id="8c5d0-101">Set-AzDataBoxEdgeShare</span><span class="sxs-lookup"><span data-stu-id="8c5d0-101">Set-AzDataBoxEdgeShare</span></span>

## <span data-ttu-id="8c5d0-102">Sammanfattning</span><span class="sxs-lookup"><span data-stu-id="8c5d0-102">SYNOPSIS</span></span>
<span data-ttu-id="8c5d0-103">Uppdaterar resursen för en enhet.</span><span class="sxs-lookup"><span data-stu-id="8c5d0-103">Updates the share for a device.</span></span>

## <span data-ttu-id="8c5d0-104">FRÅGESYNTAXEN</span><span class="sxs-lookup"><span data-stu-id="8c5d0-104">SYNTAX</span></span>

### <span data-ttu-id="8c5d0-105">SmbParameterSet (standard)</span><span class="sxs-lookup"><span data-stu-id="8c5d0-105">SmbParameterSet (Default)</span></span>
```
Set-AzDataBoxEdgeShare [-ResourceGroupName] <String> [-DeviceName] <String> [-Name] <String>
 -UserAccessRight <Hashtable[]> [-AsJob] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

### <span data-ttu-id="8c5d0-106">UpdateByResourceIdSmbParameterSet</span><span class="sxs-lookup"><span data-stu-id="8c5d0-106">UpdateByResourceIdSmbParameterSet</span></span>
```
Set-AzDataBoxEdgeShare -ResourceId <String> -UserAccessRight <Hashtable[]> [-AsJob]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="8c5d0-107">UpdateByResourceIdNfsParameterSet</span><span class="sxs-lookup"><span data-stu-id="8c5d0-107">UpdateByResourceIdNfsParameterSet</span></span>
```
Set-AzDataBoxEdgeShare -ResourceId <String> -ClientAccessRight <Hashtable[]> [-AsJob]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="8c5d0-108">UpdateByInputObjectSmbParameterSet</span><span class="sxs-lookup"><span data-stu-id="8c5d0-108">UpdateByInputObjectSmbParameterSet</span></span>
```
Set-AzDataBoxEdgeShare -InputObject <PSDataBoxEdgeShare> -UserAccessRight <Hashtable[]> [-AsJob]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="8c5d0-109">UpdateByInputObjectNfsParameterSet</span><span class="sxs-lookup"><span data-stu-id="8c5d0-109">UpdateByInputObjectNfsParameterSet</span></span>
```
Set-AzDataBoxEdgeShare -InputObject <PSDataBoxEdgeShare> -ClientAccessRight <Hashtable[]> [-AsJob]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="8c5d0-110">NfsParameterSet</span><span class="sxs-lookup"><span data-stu-id="8c5d0-110">NfsParameterSet</span></span>
```
Set-AzDataBoxEdgeShare [-ResourceGroupName] <String> [-DeviceName] <String> [-Name] <String>
 -ClientAccessRight <Hashtable[]> [-AsJob] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

## <span data-ttu-id="8c5d0-111">PROBLEMBESKRIVNING</span><span class="sxs-lookup"><span data-stu-id="8c5d0-111">DESCRIPTION</span></span>
<span data-ttu-id="8c5d0-112">Denna **set-AzDataBoxEdgeShare** ersätter åtkomst rättigheterna</span><span class="sxs-lookup"><span data-stu-id="8c5d0-112">This **Set-AzDataBoxEdgeShare** will replace the access rights</span></span>

## <span data-ttu-id="8c5d0-113">BESKRIVS</span><span class="sxs-lookup"><span data-stu-id="8c5d0-113">EXAMPLES</span></span>

### <span data-ttu-id="8c5d0-114">Exempel 1</span><span class="sxs-lookup"><span data-stu-id="8c5d0-114">Example 1</span></span>
```powershell
PS C:\> $AccessRights = @(@{"ClientId"="192.168.10.10";"AccessRight"="NoAccess"}, @{"ClientId"="192.168.10.11";"AccessRight"="ReadOnly"})
PS C:\> Set-AzDataBoxEdgeShare -ResourceGroupName resource-group-name -ClientAccessRight $AccessRights
Name       Type       DataPolicy       DataFormat       ResourceGroupName     StorageAccountName
---------- ---------- ---------------- ---------------- --------------------- -------------------
share-2    NFS        Cloud            PageBlob         resource-group-name   storage-account-name
## $ClientAccessRights = @(@{"ClientId"="192.168.10.10";"AccessRight"="NoAccess"}, @{"ClientId"="192.168.10.11";"AccessRight"="ReadOnly"})
## Possible values for AccessRight options are 'NoAccess', 'ReadOnly', 'ReadWrite'
```

### <span data-ttu-id="8c5d0-115">Exempel 2</span><span class="sxs-lookup"><span data-stu-id="8c5d0-115">Example 2</span></span>
```powershell
PS C:\> $AccessRights = @(@{"Username"="user-name-1";"AccessRight"="Read"}, @{"Username"="user-name-2";"AccessRight"="Read"}, @{"Username"="user-name-3";"AccessRight"="Custom"})
PS C:\> Set-AzDataBoxEdgeShare -ResourceGroupName resource-group-name -UserAccessRight $AccessRights
Name       Type       DataPolicy       DataFormat       ResourceGroupName     StorageAccountName
---------- ---------- ---------------- ---------------- --------------------- -------------------
share-1    SMB        Cloud            PageBlob         resource-group-name   storage-account-name
## $UserAccessRights = @(@{"Username"="user-name-1";"AccessRight"="Read"}, @{"Username"="user-name-2";"AccessRight"="Read"}, @{"Username"="user-name-3";"AccessRight"="Custom"})
## Possible values for AccessRight are 'Change', 'Read', 'Custom'
```

## <span data-ttu-id="8c5d0-116">MALLPARAMETRAR</span><span class="sxs-lookup"><span data-stu-id="8c5d0-116">PARAMETERS</span></span>

### <span data-ttu-id="8c5d0-117">-AsJob</span><span class="sxs-lookup"><span data-stu-id="8c5d0-117">-AsJob</span></span>
<span data-ttu-id="8c5d0-118">Kör cmdlet i bakgrunden</span><span class="sxs-lookup"><span data-stu-id="8c5d0-118">Run cmdlet in the background</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="8c5d0-119">-ClientAccessRight</span><span class="sxs-lookup"><span data-stu-id="8c5d0-119">-ClientAccessRight</span></span>
<span data-ttu-id="8c5d0-120">Läs-och skriv åtkomst för clientIds, till ex: @ (@ {"ClientId" = "192.168.10.10"; " AccessRight "=" noaccess "}, @ {" ClientId "=" 192.168.10.11 ";" AccessRight "=" ReadOnly "})</span><span class="sxs-lookup"><span data-stu-id="8c5d0-120">Read/Write Access for clientIds, For ex:@(@{"ClientId"="192.168.10.10";"AccessRight"="NoAccess"}, @{"ClientId"="192.168.10.11";"AccessRight"="ReadOnly"})</span></span>

```yaml
Type: System.Collections.Hashtable[]
Parameter Sets: UpdateByResourceIdNfsParameterSet, UpdateByInputObjectNfsParameterSet, NfsParameterSet
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="8c5d0-121">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="8c5d0-121">-DefaultProfile</span></span>
<span data-ttu-id="8c5d0-122">Autentiseringsuppgifter, konto, klient organisation och abonnemang som används för kommunikation med Azure.</span><span class="sxs-lookup"><span data-stu-id="8c5d0-122">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

```yaml
Type: Microsoft.Azure.Commands.Common.Authentication.Abstractions.Core.IAzureContextContainer
Parameter Sets: (All)
Aliases: AzContext, AzureRmContext, AzureCredential

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="8c5d0-123">-Enhets namn</span><span class="sxs-lookup"><span data-stu-id="8c5d0-123">-DeviceName</span></span>
<span data-ttu-id="8c5d0-124">Enhetens namn</span><span class="sxs-lookup"><span data-stu-id="8c5d0-124">Device Name</span></span>

```yaml
Type: System.String
Parameter Sets: SmbParameterSet, NfsParameterSet
Aliases:

Required: True
Position: 1
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="8c5d0-125">-InputObject</span><span class="sxs-lookup"><span data-stu-id="8c5d0-125">-InputObject</span></span>
<span data-ttu-id="8c5d0-126">Infoga objekt</span><span class="sxs-lookup"><span data-stu-id="8c5d0-126">Input Object</span></span>

```yaml
Type: Microsoft.Azure.PowerShell.Cmdlets.DataBoxEdge.Models.PSDataBoxEdgeShare
Parameter Sets: UpdateByInputObjectSmbParameterSet, UpdateByInputObjectNfsParameterSet
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="8c5d0-127">-Namn</span><span class="sxs-lookup"><span data-stu-id="8c5d0-127">-Name</span></span>
<span data-ttu-id="8c5d0-128">Resurs namn</span><span class="sxs-lookup"><span data-stu-id="8c5d0-128">Resource Name</span></span>

```yaml
Type: System.String
Parameter Sets: SmbParameterSet, NfsParameterSet
Aliases:

Required: True
Position: 2
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="8c5d0-129">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="8c5d0-129">-ResourceGroupName</span></span>
<span data-ttu-id="8c5d0-130">Resurs grupps namn</span><span class="sxs-lookup"><span data-stu-id="8c5d0-130">Resource Group Name</span></span>

```yaml
Type: System.String
Parameter Sets: SmbParameterSet, NfsParameterSet
Aliases:

Required: True
Position: 0
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="8c5d0-131">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="8c5d0-131">-ResourceId</span></span>
<span data-ttu-id="8c5d0-132">Azure ResourceId</span><span class="sxs-lookup"><span data-stu-id="8c5d0-132">Azure ResourceId</span></span>

```yaml
Type: System.String
Parameter Sets: UpdateByResourceIdSmbParameterSet, UpdateByResourceIdNfsParameterSet
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="8c5d0-133">-UserAccessRight</span><span class="sxs-lookup"><span data-stu-id="8c5d0-133">-UserAccessRight</span></span>
<span data-ttu-id="8c5d0-134">ge åtkomst direkt med befintliga användar namn för åtkomst till SMB-filtyper, till ex: @ (@ {"username" = "User-Name-1"; " AccessRight "=" Läs "}, @ {" username "=" User-Name-2 ";" AccessRight "=" Läs "}, @ {" username "=" User-Name-3 ";" AccessRight "=" Custom "})</span><span class="sxs-lookup"><span data-stu-id="8c5d0-134">provide access right along with existing usernames to access SMB Share types, For ex: @(@{"Username"="user-name-1";"AccessRight"="Read"}, @{"Username"="user-name-2";"AccessRight"="Read"}, @{"Username"="user-name-3";"AccessRight"="Custom"})</span></span>

```yaml
Type: System.Collections.Hashtable[]
Parameter Sets: SmbParameterSet, UpdateByResourceIdSmbParameterSet, UpdateByInputObjectSmbParameterSet
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="8c5d0-135">-Bekräfta</span><span class="sxs-lookup"><span data-stu-id="8c5d0-135">-Confirm</span></span>
<span data-ttu-id="8c5d0-136">Du uppmanas att bekräfta innan du kör cmdleten.</span><span class="sxs-lookup"><span data-stu-id="8c5d0-136">Prompts you for confirmation before running the cmdlet.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases: cf

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="8c5d0-137">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="8c5d0-137">-WhatIf</span></span>
<span data-ttu-id="8c5d0-138">Visar vad som händer om cmdleten körs.</span><span class="sxs-lookup"><span data-stu-id="8c5d0-138">Shows what would happen if the cmdlet runs.</span></span> <span data-ttu-id="8c5d0-139">Cmdleten körs inte.</span><span class="sxs-lookup"><span data-stu-id="8c5d0-139">The cmdlet is not run.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases: wi

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="8c5d0-140">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="8c5d0-140">CommonParameters</span></span>
<span data-ttu-id="8c5d0-141">Den här cmdleten har stöd för de gemensamma parametrarna:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-disvariable,-utbuffer,-PipelineVariable,-verbose,-WarningAction och-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="8c5d0-141">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="8c5d0-142">Mer information finns i [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="8c5d0-142">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="8c5d0-143">KOSTNADS</span><span class="sxs-lookup"><span data-stu-id="8c5d0-143">INPUTS</span></span>

### <span data-ttu-id="8c5d0-144">System. String</span><span class="sxs-lookup"><span data-stu-id="8c5d0-144">System.String</span></span>

### <span data-ttu-id="8c5d0-145">Microsoft.Azure.PowerShell.Cmdlets.DataBoxEdge.Models.PSDataBoxEdgeShare</span><span class="sxs-lookup"><span data-stu-id="8c5d0-145">Microsoft.Azure.PowerShell.Cmdlets.DataBoxEdge.Models.PSDataBoxEdgeShare</span></span>

## <span data-ttu-id="8c5d0-146">VÄRDEN</span><span class="sxs-lookup"><span data-stu-id="8c5d0-146">OUTPUTS</span></span>

### <span data-ttu-id="8c5d0-147">Microsoft.Azure.PowerShell.Cmdlets.DataBoxEdge.Models.PSDataBoxEdgeShare</span><span class="sxs-lookup"><span data-stu-id="8c5d0-147">Microsoft.Azure.PowerShell.Cmdlets.DataBoxEdge.Models.PSDataBoxEdgeShare</span></span>

## <span data-ttu-id="8c5d0-148">ANMÄRKNINGAR</span><span class="sxs-lookup"><span data-stu-id="8c5d0-148">NOTES</span></span>

## <span data-ttu-id="8c5d0-149">RELATERADE LÄNKAR</span><span class="sxs-lookup"><span data-stu-id="8c5d0-149">RELATED LINKS</span></span>