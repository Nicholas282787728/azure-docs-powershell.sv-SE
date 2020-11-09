---
external help file: Microsoft.Azure.PowerShell.Cmdlets.StorageSync.dll-Help.xml
Module Name: Az.StorageSync
online version: https://docs.microsoft.com/en-us/powershell/module/Az.storagesync/new-Azstoragesynccloudendpoint
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/StorageSync/StorageSync/help/New-AzStorageSyncCloudEndpoint.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/StorageSync/StorageSync/help/New-AzStorageSyncCloudEndpoint.md
ms.openlocfilehash: 95b30bda3d824fccc5bb40e442697b81b6396d56
ms.sourcegitcommit: b4a38bcb0501a9016a4998efd377aa75d3ef9ce8
ms.translationtype: MT
ms.contentlocale: sv-SE
ms.lasthandoff: 10/27/2020
ms.locfileid: "94324912"
---
# <span data-ttu-id="5891f-101">New-AzStorageSyncCloudEndpoint</span><span class="sxs-lookup"><span data-stu-id="5891f-101">New-AzStorageSyncCloudEndpoint</span></span>

## <span data-ttu-id="5891f-102">Sammanfattning</span><span class="sxs-lookup"><span data-stu-id="5891f-102">SYNOPSIS</span></span>
<span data-ttu-id="5891f-103">Det här kommandot skapar en Azure File Sync-slutpunkt för moln i en synkroniseringsresurs.</span><span class="sxs-lookup"><span data-stu-id="5891f-103">This command creates an Azure File Sync cloud endpoint in a sync group.</span></span>

## <span data-ttu-id="5891f-104">FRÅGESYNTAXEN</span><span class="sxs-lookup"><span data-stu-id="5891f-104">SYNTAX</span></span>

### <span data-ttu-id="5891f-105">StringParameterSet (standard)</span><span class="sxs-lookup"><span data-stu-id="5891f-105">StringParameterSet (Default)</span></span>
```
New-AzStorageSyncCloudEndpoint [-ResourceGroupName] <String> [-StorageSyncServiceName] <String>
 [-SyncGroupName] <String> -Name <String> -StorageAccountResourceId <String> -AzureFileShareName <String>
 [-StorageAccountTenantId <String>] [-AsJob] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

### <span data-ttu-id="5891f-106">ObjectParameterSet</span><span class="sxs-lookup"><span data-stu-id="5891f-106">ObjectParameterSet</span></span>
```
New-AzStorageSyncCloudEndpoint [-ParentObject] <PSSyncGroup> -Name <String> -StorageAccountResourceId <String>
 -AzureFileShareName <String> [-StorageAccountTenantId <String>] [-AsJob]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="5891f-107">ParentStringParameterSet</span><span class="sxs-lookup"><span data-stu-id="5891f-107">ParentStringParameterSet</span></span>
```
New-AzStorageSyncCloudEndpoint [-ParentResourceId] <String> -Name <String> -StorageAccountResourceId <String>
 -AzureFileShareName <String> [-StorageAccountTenantId <String>] [-AsJob]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="5891f-108">PROBLEMBESKRIVNING</span><span class="sxs-lookup"><span data-stu-id="5891f-108">DESCRIPTION</span></span>
<span data-ttu-id="5891f-109">Det här kommandot skapar en Azure File Sync-slutpunkt för moln.</span><span class="sxs-lookup"><span data-stu-id="5891f-109">This command creates an Azure File Sync cloud endpoint.</span></span> <span data-ttu-id="5891f-110">En moln slut punkt är en referens till en befintlig Azure-fildelning.</span><span class="sxs-lookup"><span data-stu-id="5891f-110">A cloud endpoint is a reference to an existing Azure file share.</span></span> <span data-ttu-id="5891f-111">Den representerar fil resursen och definierar den för att synkronisera alla filer som ingår i den synkroniserade gruppen moln slut punkten har skapats i.</span><span class="sxs-lookup"><span data-stu-id="5891f-111">It represents the file share and defines it participation in syncing all the files part of the sync group the cloud endpoint has been created in.</span></span>

## <span data-ttu-id="5891f-112">BESKRIVS</span><span class="sxs-lookup"><span data-stu-id="5891f-112">EXAMPLES</span></span>

### <span data-ttu-id="5891f-113">Exempel 1</span><span class="sxs-lookup"><span data-stu-id="5891f-113">Example 1</span></span>
```powershell
PS C:\> New-AzStorageSyncCloudEndpoint -ResourceGroupName "myResourceGroup" -StorageSyncServiceName "myStorageSyncServiceName" -SyncGroupName "mySyncGroupName" -Name "myCloudEndpointName" -StorageAccountResourceId $storageAccountResourceId -AzureFileShareName "myAzureFileShareName" -StorageAccountTenantId "myStorageAccountTenantId"
```

<span data-ttu-id="5891f-114">En moln slut punkt är en integrerad medlem i en synkroniseringsresurs, det här är ett exempel på hur du skapar en i en befintlig synkroniseringsresurs med namnet "mySyncGroupName".</span><span class="sxs-lookup"><span data-stu-id="5891f-114">A cloud endpoint is an integral member of a sync group, this is an example of creating one inside of an existing sync group called "mySyncGroupName".</span></span>

## <span data-ttu-id="5891f-115">MALLPARAMETRAR</span><span class="sxs-lookup"><span data-stu-id="5891f-115">PARAMETERS</span></span>

### <span data-ttu-id="5891f-116">-AsJob</span><span class="sxs-lookup"><span data-stu-id="5891f-116">-AsJob</span></span>
<span data-ttu-id="5891f-117">Kör cmdlet i bakgrunden</span><span class="sxs-lookup"><span data-stu-id="5891f-117">Run cmdlet in the background</span></span>

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

### <span data-ttu-id="5891f-118">-AzureFileShareName</span><span class="sxs-lookup"><span data-stu-id="5891f-118">-AzureFileShareName</span></span>
<span data-ttu-id="5891f-119">Namn på lagrings konto delning (Azure-fildelnings namn)</span><span class="sxs-lookup"><span data-stu-id="5891f-119">Storage Account Share Name (Azure file share name)</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases: StorageAccountShareName

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="5891f-120">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="5891f-120">-DefaultProfile</span></span>
<span data-ttu-id="5891f-121">Autentiseringsuppgifter, konto, klient organisation och abonnemang som används för kommunikation med Azure.</span><span class="sxs-lookup"><span data-stu-id="5891f-121">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="5891f-122">-Namn</span><span class="sxs-lookup"><span data-stu-id="5891f-122">-Name</span></span>
<span data-ttu-id="5891f-123">Namnet på moln slut punkten.</span><span class="sxs-lookup"><span data-stu-id="5891f-123">Name of the cloud endpoint.</span></span> <span data-ttu-id="5891f-124">När du skapar ett namn via Azure-portalen anges namnet på den Azure-fildelning som den refererar till.</span><span class="sxs-lookup"><span data-stu-id="5891f-124">When created through the Azure portal, Name is set to the name of the Azure file share it references.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases: CloudEndpointName

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="5891f-125">-ParentObject</span><span class="sxs-lookup"><span data-stu-id="5891f-125">-ParentObject</span></span>
<span data-ttu-id="5891f-126">SyncGroup-objekt som normalt passerar genom parametern.</span><span class="sxs-lookup"><span data-stu-id="5891f-126">SyncGroup Object, normally passed through the parameter.</span></span>

```yaml
Type: Microsoft.Azure.Commands.StorageSync.Models.PSSyncGroup
Parameter Sets: ObjectParameterSet
Aliases: SyncGroup

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="5891f-127">-ParentResourceId</span><span class="sxs-lookup"><span data-stu-id="5891f-127">-ParentResourceId</span></span>
<span data-ttu-id="5891f-128">Överordnat resurs-ID för SyncGroup</span><span class="sxs-lookup"><span data-stu-id="5891f-128">SyncGroup Parent Resource Id</span></span>

```yaml
Type: System.String
Parameter Sets: ParentStringParameterSet
Aliases: SyncGroupId

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="5891f-129">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="5891f-129">-ResourceGroupName</span></span>
<span data-ttu-id="5891f-130">Resurs grupps namn.</span><span class="sxs-lookup"><span data-stu-id="5891f-130">Resource Group Name.</span></span>

```yaml
Type: System.String
Parameter Sets: StringParameterSet
Aliases:

Required: True
Position: 0
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="5891f-131">-StorageAccountResourceId</span><span class="sxs-lookup"><span data-stu-id="5891f-131">-StorageAccountResourceId</span></span>
<span data-ttu-id="5891f-132">Resurs-ID för lagrings konto</span><span class="sxs-lookup"><span data-stu-id="5891f-132">Storage Account Resource Id</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="5891f-133">-StorageAccountTenantId</span><span class="sxs-lookup"><span data-stu-id="5891f-133">-StorageAccountTenantId</span></span>
<span data-ttu-id="5891f-134">ID för klient organisations konto (företags katalog-ID)</span><span class="sxs-lookup"><span data-stu-id="5891f-134">Storage Account Tenant Id (Company Directory Id)</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="5891f-135">-StorageSyncServiceName</span><span class="sxs-lookup"><span data-stu-id="5891f-135">-StorageSyncServiceName</span></span>
<span data-ttu-id="5891f-136">Namn på StorageSyncService.</span><span class="sxs-lookup"><span data-stu-id="5891f-136">Name of the StorageSyncService.</span></span>

```yaml
Type: System.String
Parameter Sets: StringParameterSet
Aliases: ParentName

Required: True
Position: 1
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="5891f-137">-SyncGroupName</span><span class="sxs-lookup"><span data-stu-id="5891f-137">-SyncGroupName</span></span>
<span data-ttu-id="5891f-138">Namn på SyncGroup.</span><span class="sxs-lookup"><span data-stu-id="5891f-138">Name of the SyncGroup.</span></span>

```yaml
Type: System.String
Parameter Sets: StringParameterSet
Aliases:

Required: True
Position: 2
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="5891f-139">-Bekräfta</span><span class="sxs-lookup"><span data-stu-id="5891f-139">-Confirm</span></span>
<span data-ttu-id="5891f-140">Du uppmanas att bekräfta innan du kör cmdleten.</span><span class="sxs-lookup"><span data-stu-id="5891f-140">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="5891f-141">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="5891f-141">-WhatIf</span></span>
<span data-ttu-id="5891f-142">Visar vad som händer om cmdleten körs.</span><span class="sxs-lookup"><span data-stu-id="5891f-142">Shows what would happen if the cmdlet runs.</span></span> <span data-ttu-id="5891f-143">Cmdleten körs inte.</span><span class="sxs-lookup"><span data-stu-id="5891f-143">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="5891f-144">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="5891f-144">CommonParameters</span></span>
<span data-ttu-id="5891f-145">Den här cmdleten har stöd för de gemensamma parametrarna:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-disvariable,-utbuffer,-PipelineVariable,-verbose,-WarningAction och-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="5891f-145">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="5891f-146">Mer information finns i about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="5891f-146">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="5891f-147">KOSTNADS</span><span class="sxs-lookup"><span data-stu-id="5891f-147">INPUTS</span></span>

### <span data-ttu-id="5891f-148">Microsoft. Azure. commands. StorageSync. Models. PSSyncGroup</span><span class="sxs-lookup"><span data-stu-id="5891f-148">Microsoft.Azure.Commands.StorageSync.Models.PSSyncGroup</span></span>

### <span data-ttu-id="5891f-149">System. String</span><span class="sxs-lookup"><span data-stu-id="5891f-149">System.String</span></span>

## <span data-ttu-id="5891f-150">VÄRDEN</span><span class="sxs-lookup"><span data-stu-id="5891f-150">OUTPUTS</span></span>

### <span data-ttu-id="5891f-151">Microsoft. Azure. commands. StorageSync. Models. PSCloudEndpoint</span><span class="sxs-lookup"><span data-stu-id="5891f-151">Microsoft.Azure.Commands.StorageSync.Models.PSCloudEndpoint</span></span>

## <span data-ttu-id="5891f-152">ANMÄRKNINGAR</span><span class="sxs-lookup"><span data-stu-id="5891f-152">NOTES</span></span>

## <span data-ttu-id="5891f-153">RELATERADE LÄNKAR</span><span class="sxs-lookup"><span data-stu-id="5891f-153">RELATED LINKS</span></span>
