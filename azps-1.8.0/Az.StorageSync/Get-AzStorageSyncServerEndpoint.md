---
external help file: Microsoft.Azure.Commands.StorageSync.dll-Help.xml
Module Name: Az.StorageSync
online version: https://docs.microsoft.com/en-us/powershell/module/Az.storagesync/get-Azstoragesyncserverendpoint
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/StorageSync/StorageSync/help/Get-AzStorageSyncServerEndpoint.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/StorageSync/StorageSync/help/Get-AzStorageSyncServerEndpoint.md
ms.openlocfilehash: b71da416d7609f05d4716090dc8f09bf0ec0b084
ms.sourcegitcommit: 4d2c178cd6df9151877b08d54c1f4a228dbec9d1
ms.translationtype: MT
ms.contentlocale: sv-SE
ms.lasthandoff: 01/29/2020
ms.locfileid: "93746226"
---
# <span data-ttu-id="46ecb-101">Get-AzStorageSyncServerEndpoint</span><span class="sxs-lookup"><span data-stu-id="46ecb-101">Get-AzStorageSyncServerEndpoint</span></span>

## <span data-ttu-id="46ecb-102">Sammanfattning</span><span class="sxs-lookup"><span data-stu-id="46ecb-102">SYNOPSIS</span></span>
<span data-ttu-id="46ecb-103">Det här kommandot visar alla Server slut punkter i en given synkroniseringskoppling.</span><span class="sxs-lookup"><span data-stu-id="46ecb-103">This command lists all server endpoints within a given sync group.</span></span>

## <span data-ttu-id="46ecb-104">FRÅGESYNTAXEN</span><span class="sxs-lookup"><span data-stu-id="46ecb-104">SYNTAX</span></span>

### <span data-ttu-id="46ecb-105">ObjectParameterSet (standard)</span><span class="sxs-lookup"><span data-stu-id="46ecb-105">ObjectParameterSet (Default)</span></span>
```
Get-AzStorageSyncServerEndpoint [-ParentObject] <PSSyncGroup> [-Name <String>]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="46ecb-106">StringParameterSet</span><span class="sxs-lookup"><span data-stu-id="46ecb-106">StringParameterSet</span></span>
```
Get-AzStorageSyncServerEndpoint [-ResourceGroupName] <String> [-StorageSyncServiceName] <String>
 [-SyncGroupName] <String> [-Name <String>] [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="46ecb-107">ParentStringParameterSet</span><span class="sxs-lookup"><span data-stu-id="46ecb-107">ParentStringParameterSet</span></span>
```
Get-AzStorageSyncServerEndpoint [-ParentResourceId] <String> [-Name <String>]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="46ecb-108">PROBLEMBESKRIVNING</span><span class="sxs-lookup"><span data-stu-id="46ecb-108">DESCRIPTION</span></span>
<span data-ttu-id="46ecb-109">Det här kommandot visar alla Server slut punkter i en given synkroniseringskoppling.</span><span class="sxs-lookup"><span data-stu-id="46ecb-109">This command lists all server endpoints within a given sync group.</span></span> <span data-ttu-id="46ecb-110">Den kan också användas för att lista attributen för varje server slut punkt.</span><span class="sxs-lookup"><span data-stu-id="46ecb-110">It can be used to also list the attributes of each server endpoint.</span></span>

## <span data-ttu-id="46ecb-111">BESKRIVS</span><span class="sxs-lookup"><span data-stu-id="46ecb-111">EXAMPLES</span></span>

### <span data-ttu-id="46ecb-112">Exempel 1</span><span class="sxs-lookup"><span data-stu-id="46ecb-112">Example 1</span></span>
```powershell
PS C:\> Get-AzStorageSyncServerEndpoint -ResourceGroupName "myResourceGroup" -StorageSyncServiceName "myStorageSyncServiceName" -SyncGroupName "mySyncGroupName"
```

<span data-ttu-id="46ecb-113">Det här kommandot får alla Server slut punkter i den angivna synkroniseringsresursen.</span><span class="sxs-lookup"><span data-stu-id="46ecb-113">This command gets all server endpoints contained within the specified sync group.</span></span> <span data-ttu-id="46ecb-114">Ange-ServerEndpointName för att returnera ett specifikt nummer.</span><span class="sxs-lookup"><span data-stu-id="46ecb-114">Specify -ServerEndpointName to return a specific one.</span></span>

## <span data-ttu-id="46ecb-115">MALLPARAMETRAR</span><span class="sxs-lookup"><span data-stu-id="46ecb-115">PARAMETERS</span></span>

### <span data-ttu-id="46ecb-116">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="46ecb-116">-DefaultProfile</span></span>
<span data-ttu-id="46ecb-117">Autentiseringsuppgifter, konto, klient organisation och abonnemang som används för kommunikation med Azure.</span><span class="sxs-lookup"><span data-stu-id="46ecb-117">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="46ecb-118">-Namn</span><span class="sxs-lookup"><span data-stu-id="46ecb-118">-Name</span></span>
<span data-ttu-id="46ecb-119">Namnet på Server slut punkten.</span><span class="sxs-lookup"><span data-stu-id="46ecb-119">Name of the server endpoint.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases: ServerEndpointName

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="46ecb-120">-ParentObject</span><span class="sxs-lookup"><span data-stu-id="46ecb-120">-ParentObject</span></span>
<span data-ttu-id="46ecb-121">StorageSyncService-objekt som normalt passerar genom parametern.</span><span class="sxs-lookup"><span data-stu-id="46ecb-121">StorageSyncService Object, normally passed through the parameter.</span></span>

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

### <span data-ttu-id="46ecb-122">-ParentResourceId</span><span class="sxs-lookup"><span data-stu-id="46ecb-122">-ParentResourceId</span></span>
<span data-ttu-id="46ecb-123">StorageSyncService-objekt som normalt passerar genom parametern.</span><span class="sxs-lookup"><span data-stu-id="46ecb-123">StorageSyncService Object, normally passed through the parameter.</span></span>

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

### <span data-ttu-id="46ecb-124">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="46ecb-124">-ResourceGroupName</span></span>
<span data-ttu-id="46ecb-125">Resurs grupps namn.</span><span class="sxs-lookup"><span data-stu-id="46ecb-125">Resource Group Name.</span></span>

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

### <span data-ttu-id="46ecb-126">-StorageSyncServiceName</span><span class="sxs-lookup"><span data-stu-id="46ecb-126">-StorageSyncServiceName</span></span>
<span data-ttu-id="46ecb-127">Namn på StorageSyncService.</span><span class="sxs-lookup"><span data-stu-id="46ecb-127">Name of the StorageSyncService.</span></span>

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

### <span data-ttu-id="46ecb-128">-SyncGroupName</span><span class="sxs-lookup"><span data-stu-id="46ecb-128">-SyncGroupName</span></span>
<span data-ttu-id="46ecb-129">Namn på SyncGroup.</span><span class="sxs-lookup"><span data-stu-id="46ecb-129">Name of the SyncGroup.</span></span>

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

### <span data-ttu-id="46ecb-130">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="46ecb-130">CommonParameters</span></span>
<span data-ttu-id="46ecb-131">Den här cmdleten har stöd för de gemensamma parametrarna:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-disvariable,-utbuffer,-PipelineVariable,-verbose,-WarningAction och-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="46ecb-131">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="46ecb-132">Mer information finns i about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="46ecb-132">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="46ecb-133">KOSTNADS</span><span class="sxs-lookup"><span data-stu-id="46ecb-133">INPUTS</span></span>

### <span data-ttu-id="46ecb-134">Microsoft. Azure. commands. StorageSync. Models. PSSyncGroup</span><span class="sxs-lookup"><span data-stu-id="46ecb-134">Microsoft.Azure.Commands.StorageSync.Models.PSSyncGroup</span></span>

### <span data-ttu-id="46ecb-135">System. String</span><span class="sxs-lookup"><span data-stu-id="46ecb-135">System.String</span></span>

## <span data-ttu-id="46ecb-136">VÄRDEN</span><span class="sxs-lookup"><span data-stu-id="46ecb-136">OUTPUTS</span></span>

### <span data-ttu-id="46ecb-137">Microsoft. Azure. commands. StorageSync. Models. PSServerEndpoint</span><span class="sxs-lookup"><span data-stu-id="46ecb-137">Microsoft.Azure.Commands.StorageSync.Models.PSServerEndpoint</span></span>

## <span data-ttu-id="46ecb-138">ANMÄRKNINGAR</span><span class="sxs-lookup"><span data-stu-id="46ecb-138">NOTES</span></span>

## <span data-ttu-id="46ecb-139">RELATERADE LÄNKAR</span><span class="sxs-lookup"><span data-stu-id="46ecb-139">RELATED LINKS</span></span>
