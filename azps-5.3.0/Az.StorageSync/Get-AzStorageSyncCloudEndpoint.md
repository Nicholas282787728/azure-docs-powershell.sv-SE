---
external help file: Microsoft.Azure.PowerShell.Cmdlets.StorageSync.dll-Help.xml
Module Name: Az.StorageSync
online version: https://docs.microsoft.com/en-us/powershell/module/Az.storagesync/get-Azstoragesynccloudendpoint
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/StorageSync/StorageSync/help/Get-AzStorageSyncCloudEndpoint.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/StorageSync/StorageSync/help/Get-AzStorageSyncCloudEndpoint.md
ms.openlocfilehash: 076a1393365e93a8008f15137d078a49491d81f2
ms.sourcegitcommit: 68451baa389791703e666d95469602c5652609ee
ms.translationtype: MT
ms.contentlocale: sv-SE
ms.lasthandoff: 01/05/2021
ms.locfileid: "98419880"
---
# <span data-ttu-id="b07eb-101">Get-AzStorageSyncCloudEndpoint</span><span class="sxs-lookup"><span data-stu-id="b07eb-101">Get-AzStorageSyncCloudEndpoint</span></span>

## <span data-ttu-id="b07eb-102">Sammanfattning</span><span class="sxs-lookup"><span data-stu-id="b07eb-102">SYNOPSIS</span></span>
<span data-ttu-id="b07eb-103">Det här kommandot visar alla moln slut punkter i en given synkroniseringskoppling.</span><span class="sxs-lookup"><span data-stu-id="b07eb-103">This command lists all cloud endpoints within a given sync group.</span></span>

## <span data-ttu-id="b07eb-104">FRÅGESYNTAXEN</span><span class="sxs-lookup"><span data-stu-id="b07eb-104">SYNTAX</span></span>

### <span data-ttu-id="b07eb-105">StringParameterSet (standard)</span><span class="sxs-lookup"><span data-stu-id="b07eb-105">StringParameterSet (Default)</span></span>
```
Get-AzStorageSyncCloudEndpoint [-ResourceGroupName] <String> [-StorageSyncServiceName] <String>
 [-SyncGroupName] <String> [-Name <String>] [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="b07eb-106">ObjectParameterSet</span><span class="sxs-lookup"><span data-stu-id="b07eb-106">ObjectParameterSet</span></span>
```
Get-AzStorageSyncCloudEndpoint [-ParentObject] <PSSyncGroup> [-Name <String>]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="b07eb-107">ParentStringParameterSet</span><span class="sxs-lookup"><span data-stu-id="b07eb-107">ParentStringParameterSet</span></span>
```
Get-AzStorageSyncCloudEndpoint [-ParentResourceId] <String> [-Name <String>]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="b07eb-108">PROBLEMBESKRIVNING</span><span class="sxs-lookup"><span data-stu-id="b07eb-108">DESCRIPTION</span></span>
<span data-ttu-id="b07eb-109">Det här kommandot visar alla moln slut punkter i en given synkroniseringskoppling.</span><span class="sxs-lookup"><span data-stu-id="b07eb-109">This command lists all cloud endpoints within a given sync group.</span></span> <span data-ttu-id="b07eb-110">Den kan också användas för att lista attributen för varje moln slut punkt.</span><span class="sxs-lookup"><span data-stu-id="b07eb-110">It can be used to also list the attributes of each cloud endpoint.</span></span>

## <span data-ttu-id="b07eb-111">BESKRIVS</span><span class="sxs-lookup"><span data-stu-id="b07eb-111">EXAMPLES</span></span>

### <span data-ttu-id="b07eb-112">Exempel 1</span><span class="sxs-lookup"><span data-stu-id="b07eb-112">Example 1</span></span>
```powershell
PS C:\> Get-AzStorageSyncCloudEndpoint -ResourceGroupName "myResourceGroup" -StorageSyncServiceName "myStorageSyncServiceName" -SyncGroupName "mySyncGroupName"
```

<span data-ttu-id="b07eb-113">Det här kommandot får alla moln slut punkter i den angivna synkroniseringsresursen.</span><span class="sxs-lookup"><span data-stu-id="b07eb-113">This command gets all cloud endpoints contained within the specified sync group.</span></span> <span data-ttu-id="b07eb-114">Ange-CloudEndpointName för att returnera ett specifikt nummer.</span><span class="sxs-lookup"><span data-stu-id="b07eb-114">Specify -CloudEndpointName to return a specific one.</span></span>

## <span data-ttu-id="b07eb-115">MALLPARAMETRAR</span><span class="sxs-lookup"><span data-stu-id="b07eb-115">PARAMETERS</span></span>

### <span data-ttu-id="b07eb-116">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="b07eb-116">-DefaultProfile</span></span>
<span data-ttu-id="b07eb-117">Autentiseringsuppgifter, konto, klient organisation och abonnemang som används för kommunikation med Azure.</span><span class="sxs-lookup"><span data-stu-id="b07eb-117">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="b07eb-118">-Namn</span><span class="sxs-lookup"><span data-stu-id="b07eb-118">-Name</span></span>
<span data-ttu-id="b07eb-119">Namn på CloudEndpoint.</span><span class="sxs-lookup"><span data-stu-id="b07eb-119">Name of the CloudEndpoint.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases: CloudEndpointName

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="b07eb-120">-ParentObject</span><span class="sxs-lookup"><span data-stu-id="b07eb-120">-ParentObject</span></span>
<span data-ttu-id="b07eb-121">StorageSyncService-objekt som normalt passerar genom parametern.</span><span class="sxs-lookup"><span data-stu-id="b07eb-121">StorageSyncService Object, normally passed through the parameter.</span></span>

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

### <span data-ttu-id="b07eb-122">-ParentResourceId</span><span class="sxs-lookup"><span data-stu-id="b07eb-122">-ParentResourceId</span></span>
<span data-ttu-id="b07eb-123">StorageSyncService-objekt som normalt passerar genom parametern.</span><span class="sxs-lookup"><span data-stu-id="b07eb-123">StorageSyncService Object, normally passed through the parameter.</span></span>

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

### <span data-ttu-id="b07eb-124">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="b07eb-124">-ResourceGroupName</span></span>
<span data-ttu-id="b07eb-125">Resurs grupps namn.</span><span class="sxs-lookup"><span data-stu-id="b07eb-125">Resource Group Name.</span></span>

```yaml
Type: System.String
Parameter Sets: StringParameterSet
Aliases:

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="b07eb-126">-StorageSyncServiceName</span><span class="sxs-lookup"><span data-stu-id="b07eb-126">-StorageSyncServiceName</span></span>
<span data-ttu-id="b07eb-127">Namn på StorageSyncService.</span><span class="sxs-lookup"><span data-stu-id="b07eb-127">Name of the StorageSyncService.</span></span>

```yaml
Type: System.String
Parameter Sets: StringParameterSet
Aliases: ParentName

Required: True
Position: 1
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="b07eb-128">-SyncGroupName</span><span class="sxs-lookup"><span data-stu-id="b07eb-128">-SyncGroupName</span></span>
<span data-ttu-id="b07eb-129">Namn på SyncGroup.</span><span class="sxs-lookup"><span data-stu-id="b07eb-129">Name of the SyncGroup.</span></span>

```yaml
Type: System.String
Parameter Sets: StringParameterSet
Aliases:

Required: True
Position: 2
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="b07eb-130">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="b07eb-130">CommonParameters</span></span>
<span data-ttu-id="b07eb-131">Den här cmdleten har stöd för de gemensamma parametrarna:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-disvariable,-utbuffer,-PipelineVariable,-verbose,-WarningAction och-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="b07eb-131">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="b07eb-132">Mer information finns i about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="b07eb-132">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="b07eb-133">KOSTNADS</span><span class="sxs-lookup"><span data-stu-id="b07eb-133">INPUTS</span></span>

### <span data-ttu-id="b07eb-134">System. String</span><span class="sxs-lookup"><span data-stu-id="b07eb-134">System.String</span></span>

### <span data-ttu-id="b07eb-135">Microsoft. Azure. commands. StorageSync. Models. PSSyncGroup</span><span class="sxs-lookup"><span data-stu-id="b07eb-135">Microsoft.Azure.Commands.StorageSync.Models.PSSyncGroup</span></span>

## <span data-ttu-id="b07eb-136">VÄRDEN</span><span class="sxs-lookup"><span data-stu-id="b07eb-136">OUTPUTS</span></span>

### <span data-ttu-id="b07eb-137">Microsoft. Azure. commands. StorageSync. Models. PSCloudEndpoint</span><span class="sxs-lookup"><span data-stu-id="b07eb-137">Microsoft.Azure.Commands.StorageSync.Models.PSCloudEndpoint</span></span>

## <span data-ttu-id="b07eb-138">ANMÄRKNINGAR</span><span class="sxs-lookup"><span data-stu-id="b07eb-138">NOTES</span></span>

## <span data-ttu-id="b07eb-139">RELATERADE LÄNKAR</span><span class="sxs-lookup"><span data-stu-id="b07eb-139">RELATED LINKS</span></span>
