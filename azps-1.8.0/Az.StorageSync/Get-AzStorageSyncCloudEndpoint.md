---
external help file: Microsoft.Azure.Commands.StorageSync.dll-Help.xml
Module Name: Az.StorageSync
online version: https://docs.microsoft.com/en-us/powershell/module/Az.storagesync/get-Azstoragesynccloudendpoint
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/StorageSync/StorageSync/help/Get-AzStorageSyncCloudEndpoint.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/StorageSync/StorageSync/help/Get-AzStorageSyncCloudEndpoint.md
ms.openlocfilehash: decf935cd61c052e2e77dd8fd2eadacd7a548974
ms.sourcegitcommit: 4d2c178cd6df9151877b08d54c1f4a228dbec9d1
ms.translationtype: MT
ms.contentlocale: sv-SE
ms.lasthandoff: 01/29/2020
ms.locfileid: "93746231"
---
# <span data-ttu-id="07e98-101">Get-AzStorageSyncCloudEndpoint</span><span class="sxs-lookup"><span data-stu-id="07e98-101">Get-AzStorageSyncCloudEndpoint</span></span>

## <span data-ttu-id="07e98-102">Sammanfattning</span><span class="sxs-lookup"><span data-stu-id="07e98-102">SYNOPSIS</span></span>
<span data-ttu-id="07e98-103">Det här kommandot visar alla moln slut punkter i en given synkroniseringskoppling.</span><span class="sxs-lookup"><span data-stu-id="07e98-103">This command lists all cloud endpoints within a given sync group.</span></span>

## <span data-ttu-id="07e98-104">FRÅGESYNTAXEN</span><span class="sxs-lookup"><span data-stu-id="07e98-104">SYNTAX</span></span>

### <span data-ttu-id="07e98-105">ObjectParameterSet (standard)</span><span class="sxs-lookup"><span data-stu-id="07e98-105">ObjectParameterSet (Default)</span></span>
```
Get-AzStorageSyncCloudEndpoint [-ParentObject] <PSSyncGroup> [-Name <String>]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="07e98-106">StringParameterSet</span><span class="sxs-lookup"><span data-stu-id="07e98-106">StringParameterSet</span></span>
```
Get-AzStorageSyncCloudEndpoint [-ResourceGroupName] <String> [-StorageSyncServiceName] <String>
 [-SyncGroupName] <String> [-Name <String>] [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="07e98-107">ParentStringParameterSet</span><span class="sxs-lookup"><span data-stu-id="07e98-107">ParentStringParameterSet</span></span>
```
Get-AzStorageSyncCloudEndpoint [-ParentResourceId] <String> [-Name <String>]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="07e98-108">PROBLEMBESKRIVNING</span><span class="sxs-lookup"><span data-stu-id="07e98-108">DESCRIPTION</span></span>
<span data-ttu-id="07e98-109">Det här kommandot visar alla moln slut punkter i en given synkroniseringskoppling.</span><span class="sxs-lookup"><span data-stu-id="07e98-109">This command lists all cloud endpoints within a given sync group.</span></span> <span data-ttu-id="07e98-110">Den kan också användas för att lista attributen för varje moln slut punkt.</span><span class="sxs-lookup"><span data-stu-id="07e98-110">It can be used to also list the attributes of each cloud endpoint.</span></span>

## <span data-ttu-id="07e98-111">BESKRIVS</span><span class="sxs-lookup"><span data-stu-id="07e98-111">EXAMPLES</span></span>

### <span data-ttu-id="07e98-112">Exempel 1</span><span class="sxs-lookup"><span data-stu-id="07e98-112">Example 1</span></span>
```powershell
PS C:\> Get-AzStorageSyncCloudEndpoint -ResourceGroupName "myResourceGroup" -StorageSyncServiceName "myStorageSyncServiceName" -SyncGroupName "mySyncGroupName"
```

<span data-ttu-id="07e98-113">Det här kommandot får alla moln slut punkter i den angivna synkroniseringsresursen.</span><span class="sxs-lookup"><span data-stu-id="07e98-113">This command gets all cloud endpoints contained within the specified sync group.</span></span> <span data-ttu-id="07e98-114">Ange-CloudEndpointName för att returnera ett specifikt nummer.</span><span class="sxs-lookup"><span data-stu-id="07e98-114">Specify -CloudEndpointName to return a specific one.</span></span>

## <span data-ttu-id="07e98-115">MALLPARAMETRAR</span><span class="sxs-lookup"><span data-stu-id="07e98-115">PARAMETERS</span></span>

### <span data-ttu-id="07e98-116">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="07e98-116">-DefaultProfile</span></span>
<span data-ttu-id="07e98-117">Autentiseringsuppgifter, konto, klient organisation och abonnemang som används för kommunikation med Azure.</span><span class="sxs-lookup"><span data-stu-id="07e98-117">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

```yaml
Type: Microsoft.Azure.Commands.Common.Authentication.Abstractions.Core.IAzureContextContainer
Parameter Sets: (All)
Aliases: AzureRmContext, AzureCredential

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="07e98-118">-Namn</span><span class="sxs-lookup"><span data-stu-id="07e98-118">-Name</span></span>
<span data-ttu-id="07e98-119">Namn på CloudEndpoint.</span><span class="sxs-lookup"><span data-stu-id="07e98-119">Name of the CloudEndpoint.</span></span>

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

### <span data-ttu-id="07e98-120">-ParentObject</span><span class="sxs-lookup"><span data-stu-id="07e98-120">-ParentObject</span></span>
<span data-ttu-id="07e98-121">StorageSyncService-objekt som normalt passerar genom parametern.</span><span class="sxs-lookup"><span data-stu-id="07e98-121">StorageSyncService Object, normally passed through the parameter.</span></span>

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

### <span data-ttu-id="07e98-122">-ParentResourceId</span><span class="sxs-lookup"><span data-stu-id="07e98-122">-ParentResourceId</span></span>
<span data-ttu-id="07e98-123">StorageSyncService-objekt som normalt passerar genom parametern.</span><span class="sxs-lookup"><span data-stu-id="07e98-123">StorageSyncService Object, normally passed through the parameter.</span></span>

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

### <span data-ttu-id="07e98-124">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="07e98-124">-ResourceGroupName</span></span>
<span data-ttu-id="07e98-125">Resurs grupps namn.</span><span class="sxs-lookup"><span data-stu-id="07e98-125">Resource Group Name.</span></span>

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

### <span data-ttu-id="07e98-126">-StorageSyncServiceName</span><span class="sxs-lookup"><span data-stu-id="07e98-126">-StorageSyncServiceName</span></span>
<span data-ttu-id="07e98-127">Namn på StorageSyncService.</span><span class="sxs-lookup"><span data-stu-id="07e98-127">Name of the StorageSyncService.</span></span>

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

### <span data-ttu-id="07e98-128">-SyncGroupName</span><span class="sxs-lookup"><span data-stu-id="07e98-128">-SyncGroupName</span></span>
<span data-ttu-id="07e98-129">Namn på SyncGroup.</span><span class="sxs-lookup"><span data-stu-id="07e98-129">Name of the SyncGroup.</span></span>

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

### <span data-ttu-id="07e98-130">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="07e98-130">CommonParameters</span></span>
<span data-ttu-id="07e98-131">Den här cmdleten har stöd för de gemensamma parametrarna:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-disvariable,-utbuffer,-PipelineVariable,-verbose,-WarningAction och-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="07e98-131">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="07e98-132">Mer information finns i about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="07e98-132">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="07e98-133">KOSTNADS</span><span class="sxs-lookup"><span data-stu-id="07e98-133">INPUTS</span></span>

### <span data-ttu-id="07e98-134">System. String</span><span class="sxs-lookup"><span data-stu-id="07e98-134">System.String</span></span>

### <span data-ttu-id="07e98-135">Microsoft. Azure. commands. StorageSync. Models. PSSyncGroup</span><span class="sxs-lookup"><span data-stu-id="07e98-135">Microsoft.Azure.Commands.StorageSync.Models.PSSyncGroup</span></span>

## <span data-ttu-id="07e98-136">VÄRDEN</span><span class="sxs-lookup"><span data-stu-id="07e98-136">OUTPUTS</span></span>

### <span data-ttu-id="07e98-137">Microsoft. Azure. commands. StorageSync. Models. PSCloudEndpoint</span><span class="sxs-lookup"><span data-stu-id="07e98-137">Microsoft.Azure.Commands.StorageSync.Models.PSCloudEndpoint</span></span>

## <span data-ttu-id="07e98-138">ANMÄRKNINGAR</span><span class="sxs-lookup"><span data-stu-id="07e98-138">NOTES</span></span>

## <span data-ttu-id="07e98-139">RELATERADE LÄNKAR</span><span class="sxs-lookup"><span data-stu-id="07e98-139">RELATED LINKS</span></span>
