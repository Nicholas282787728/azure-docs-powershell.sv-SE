---
external help file: Microsoft.Azure.PowerShell.Cmdlets.StackEdge.dll-Help.xml
Module Name: Az.StackEdge
online version: https://docs.microsoft.com/en-us/powershell/module/az.stackedge/new-azstackedgeshare
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/StackEdge/StackEdge/help/New-AzStackEdgeShare.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/StackEdge/StackEdge/help/New-AzStackEdgeShare.md
ms.openlocfilehash: 12ab6c1948f0864c7dcb930d0a658088fd83262c
ms.sourcegitcommit: 6a91b4c545350d316d3cf8c62f384478e3f3ba24
ms.translationtype: MT
ms.contentlocale: sv-SE
ms.lasthandoff: 04/21/2020
ms.locfileid: "94090794"
---
# <span data-ttu-id="cd15f-101">New-AzStackEdgeShare</span><span class="sxs-lookup"><span data-stu-id="cd15f-101">New-AzStackEdgeShare</span></span>

## <span data-ttu-id="cd15f-102">Sammanfattning</span><span class="sxs-lookup"><span data-stu-id="cd15f-102">SYNOPSIS</span></span>
<span data-ttu-id="cd15f-103">Skapar en ny enhet på enheten.</span><span class="sxs-lookup"><span data-stu-id="cd15f-103">Creates a new share on the device.</span></span>

## <span data-ttu-id="cd15f-104">FRÅGESYNTAXEN</span><span class="sxs-lookup"><span data-stu-id="cd15f-104">SYNTAX</span></span>

### <span data-ttu-id="cd15f-105">SmbParameterSet (standard)</span><span class="sxs-lookup"><span data-stu-id="cd15f-105">SmbParameterSet (Default)</span></span>
```
New-AzStackEdgeShare [-ResourceGroupName] <String> [-DeviceName] <String> [-Name] <String> [-SMB]
 [-UserAccessRight <Hashtable[]>] [-AsJob] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

### <span data-ttu-id="cd15f-106">CloudShareNfsParameterSet</span><span class="sxs-lookup"><span data-stu-id="cd15f-106">CloudShareNfsParameterSet</span></span>
```
New-AzStackEdgeShare [-ResourceGroupName] <String> [-DeviceName] <String> [-Name] <String>
 [-StorageAccountCredentialName] <String> [-CloudShare] -DataFormat <String> [-ContainerName <String>] [-NFS]
 [-ClientAccessRight <Hashtable[]>] [-AsJob] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

### <span data-ttu-id="cd15f-107">CloudShareSmbParameterSet</span><span class="sxs-lookup"><span data-stu-id="cd15f-107">CloudShareSmbParameterSet</span></span>
```
New-AzStackEdgeShare [-ResourceGroupName] <String> [-DeviceName] <String> [-Name] <String>
 [-StorageAccountCredentialName] <String> [-CloudShare] -DataFormat <String> [-ContainerName <String>] [-SMB]
 [-UserAccessRight <Hashtable[]>] [-AsJob] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

### <span data-ttu-id="cd15f-108">NfsParameterSet</span><span class="sxs-lookup"><span data-stu-id="cd15f-108">NfsParameterSet</span></span>
```
New-AzStackEdgeShare [-ResourceGroupName] <String> [-DeviceName] <String> [-Name] <String> [-NFS]
 [-ClientAccessRight <Hashtable[]>] [-AsJob] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

## <span data-ttu-id="cd15f-109">PROBLEMBESKRIVNING</span><span class="sxs-lookup"><span data-stu-id="cd15f-109">DESCRIPTION</span></span>
<span data-ttu-id="cd15f-110">Cmdleten **New-AzStackEdgeShare** skapar en ny resurs på stack Edge-enheten.</span><span class="sxs-lookup"><span data-stu-id="cd15f-110">The **New-AzStackEdgeShare** cmdlet creates a new share on the Stack Edge device.</span></span>

## <span data-ttu-id="cd15f-111">BESKRIVS</span><span class="sxs-lookup"><span data-stu-id="cd15f-111">EXAMPLES</span></span>

### <span data-ttu-id="cd15f-112">Exempel 1</span><span class="sxs-lookup"><span data-stu-id="cd15f-112">Example 1</span></span>
```
PS C:\> New-AzStackEdgeShare -ResourceGroupName resourceGroupName -DeviceName deviceName -Name share-1 -SMB
-StorageAccountCredentialName storageCredentialName -DataFormat PageBlob
Name       Type       DataPolicy       DataFormat       ResourceGroupName     StorageAccountName
---------- ---------- ---------------- ---------------- --------------------- -------------------
share-1    SMB        Cloud            PageBlob         resourceGroupName     storageAccountName
```

## <span data-ttu-id="cd15f-113">MALLPARAMETRAR</span><span class="sxs-lookup"><span data-stu-id="cd15f-113">PARAMETERS</span></span>

### <span data-ttu-id="cd15f-114">-AsJob</span><span class="sxs-lookup"><span data-stu-id="cd15f-114">-AsJob</span></span>
<span data-ttu-id="cd15f-115">Kör cmdlet i bakgrunden</span><span class="sxs-lookup"><span data-stu-id="cd15f-115">Run cmdlet in the background</span></span>

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

### <span data-ttu-id="cd15f-116">-ClientAccessRight</span><span class="sxs-lookup"><span data-stu-id="cd15f-116">-ClientAccessRight</span></span>
<span data-ttu-id="cd15f-117">Läs-och skriv åtkomst för clientIds, till ex: @ (@ {"ClientId" = "192.168.10.10"; " AccessRight "=" noaccess "}, @ {" ClientId "=" 192.168.10.11 ";" AccessRight "=" ReadOnly "})</span><span class="sxs-lookup"><span data-stu-id="cd15f-117">Read/Write Access for clientIds, For ex:@(@{"ClientId"="192.168.10.10";"AccessRight"="NoAccess"}, @{"ClientId"="192.168.10.11";"AccessRight"="ReadOnly"})</span></span>

```yaml
Type: System.Collections.Hashtable[]
Parameter Sets: CloudShareNfsParameterSet, NfsParameterSet
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="cd15f-118">-CloudShare</span><span class="sxs-lookup"><span data-stu-id="cd15f-118">-CloudShare</span></span>
<span data-ttu-id="cd15f-119">Ange befintligt StorageAccountCredential</span><span class="sxs-lookup"><span data-stu-id="cd15f-119">Provide existing StorageAccountCredential's Resource Name</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: CloudShareNfsParameterSet, CloudShareSmbParameterSet
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="cd15f-120">-ContainerName</span><span class="sxs-lookup"><span data-stu-id="cd15f-120">-ContainerName</span></span>
<span data-ttu-id="cd15f-121">Behållar namn (baserat på det data format som anges representerar detta namnet på Azure-filer/Pageblob/Block Blob)</span><span class="sxs-lookup"><span data-stu-id="cd15f-121">Container name (Based on the data format specified, this represents the name of Azure Files/Pageblob/Block blob)</span></span>

```yaml
Type: System.String
Parameter Sets: CloudShareNfsParameterSet, CloudShareSmbParameterSet
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="cd15f-122">-DataFormat</span><span class="sxs-lookup"><span data-stu-id="cd15f-122">-DataFormat</span></span>
<span data-ttu-id="cd15f-123">Ange data format från t ex: PageBlob, BlobBlob</span><span class="sxs-lookup"><span data-stu-id="cd15f-123">Set Data Format ex: PageBlob, BlobBlob</span></span>

```yaml
Type: System.String
Parameter Sets: CloudShareNfsParameterSet, CloudShareSmbParameterSet
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="cd15f-124">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="cd15f-124">-DefaultProfile</span></span>
<span data-ttu-id="cd15f-125">Autentiseringsuppgifter, konto, klient organisation och abonnemang som används för kommunikation med Azure.</span><span class="sxs-lookup"><span data-stu-id="cd15f-125">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="cd15f-126">-Enhets namn</span><span class="sxs-lookup"><span data-stu-id="cd15f-126">-DeviceName</span></span>
<span data-ttu-id="cd15f-127">Enhetens namn</span><span class="sxs-lookup"><span data-stu-id="cd15f-127">Device Name</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: True
Position: 1
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="cd15f-128">-Namn</span><span class="sxs-lookup"><span data-stu-id="cd15f-128">-Name</span></span>
<span data-ttu-id="cd15f-129">Resurs namn</span><span class="sxs-lookup"><span data-stu-id="cd15f-129">Resource Name</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases: EdgeShareName

Required: True
Position: 2
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="cd15f-130">-NFS</span><span class="sxs-lookup"><span data-stu-id="cd15f-130">-NFS</span></span>
<span data-ttu-id="cd15f-131">AccessProtocol om du vill skapa en resurs</span><span class="sxs-lookup"><span data-stu-id="cd15f-131">AccessProtocol in the case of creating Share</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: CloudShareNfsParameterSet, NfsParameterSet
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="cd15f-132">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="cd15f-132">-ResourceGroupName</span></span>
<span data-ttu-id="cd15f-133">Resurs grupps namn</span><span class="sxs-lookup"><span data-stu-id="cd15f-133">Resource Group Name</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="cd15f-134">-SMB</span><span class="sxs-lookup"><span data-stu-id="cd15f-134">-SMB</span></span>
<span data-ttu-id="cd15f-135">AccessProtocol om du vill skapa en resurs</span><span class="sxs-lookup"><span data-stu-id="cd15f-135">AccessProtocol in the case of creating Share</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: SmbParameterSet, CloudShareSmbParameterSet
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="cd15f-136">-StorageAccountCredentialName</span><span class="sxs-lookup"><span data-stu-id="cd15f-136">-StorageAccountCredentialName</span></span>
<span data-ttu-id="cd15f-137">Ange befintligt StorageAccountCredential</span><span class="sxs-lookup"><span data-stu-id="cd15f-137">Provide existing StorageAccountCredential's Resource Name</span></span>

```yaml
Type: System.String
Parameter Sets: CloudShareNfsParameterSet, CloudShareSmbParameterSet
Aliases:

Required: True
Position: 3
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="cd15f-138">-UserAccessRight</span><span class="sxs-lookup"><span data-stu-id="cd15f-138">-UserAccessRight</span></span>
<span data-ttu-id="cd15f-139">ge åtkomst direkt med befintliga användar namn för åtkomst till SMB-filtyper, till ex: @ (@ {"username" = "User-Name-1"; " AccessRight "=" Läs "}, @ {" username "=" User-Name-2 ";" AccessRight "=" Läs "}, @ {" username "=" User-Name-3 ";" AccessRight "=" Custom "})</span><span class="sxs-lookup"><span data-stu-id="cd15f-139">provide access right along with existing usernames to access SMB Share types, For ex: @(@{"Username"="user-name-1";"AccessRight"="Read"}, @{"Username"="user-name-2";"AccessRight"="Read"}, @{"Username"="user-name-3";"AccessRight"="Custom"})</span></span>

```yaml
Type: System.Collections.Hashtable[]
Parameter Sets: SmbParameterSet, CloudShareSmbParameterSet
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="cd15f-140">-Bekräfta</span><span class="sxs-lookup"><span data-stu-id="cd15f-140">-Confirm</span></span>
<span data-ttu-id="cd15f-141">Du uppmanas att bekräfta innan du kör cmdleten.</span><span class="sxs-lookup"><span data-stu-id="cd15f-141">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="cd15f-142">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="cd15f-142">-WhatIf</span></span>
<span data-ttu-id="cd15f-143">Visar vad som händer om cmdleten körs.</span><span class="sxs-lookup"><span data-stu-id="cd15f-143">Shows what would happen if the cmdlet runs.</span></span> <span data-ttu-id="cd15f-144">Cmdleten körs inte.</span><span class="sxs-lookup"><span data-stu-id="cd15f-144">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="cd15f-145">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="cd15f-145">CommonParameters</span></span>
<span data-ttu-id="cd15f-146">Den här cmdleten har stöd för de gemensamma parametrarna:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-disvariable,-utbuffer,-PipelineVariable,-verbose,-WarningAction och-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="cd15f-146">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="cd15f-147">Mer information finns i [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="cd15f-147">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="cd15f-148">KOSTNADS</span><span class="sxs-lookup"><span data-stu-id="cd15f-148">INPUTS</span></span>

### <span data-ttu-id="cd15f-149">System. String</span><span class="sxs-lookup"><span data-stu-id="cd15f-149">System.String</span></span>

## <span data-ttu-id="cd15f-150">VÄRDEN</span><span class="sxs-lookup"><span data-stu-id="cd15f-150">OUTPUTS</span></span>

### <span data-ttu-id="cd15f-151">Microsoft. Azure. PowerShell. cmdletar. StackEdge. Models. PSStackEdgeShare</span><span class="sxs-lookup"><span data-stu-id="cd15f-151">Microsoft.Azure.PowerShell.Cmdlets.StackEdge.Models.PSStackEdgeShare</span></span>

## <span data-ttu-id="cd15f-152">ANMÄRKNINGAR</span><span class="sxs-lookup"><span data-stu-id="cd15f-152">NOTES</span></span>

## <span data-ttu-id="cd15f-153">RELATERADE LÄNKAR</span><span class="sxs-lookup"><span data-stu-id="cd15f-153">RELATED LINKS</span></span>
