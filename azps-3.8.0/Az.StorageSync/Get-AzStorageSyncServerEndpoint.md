---
external help file: Microsoft.Azure.PowerShell.Cmdlets.StorageSync.dll-Help.xml
Module Name: Az.StorageSync
online version: https://docs.microsoft.com/en-us/powershell/module/Az.storagesync/get-Azstoragesyncserverendpoint
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/StorageSync/StorageSync/help/Get-AzStorageSyncServerEndpoint.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/StorageSync/StorageSync/help/Get-AzStorageSyncServerEndpoint.md
ms.openlocfilehash: 35a3e8c3eecfe8e710addde0eb2080aa20333f0b
ms.sourcegitcommit: 6a91b4c545350d316d3cf8c62f384478e3f3ba24
ms.translationtype: MT
ms.contentlocale: sv-SE
ms.lasthandoff: 04/21/2020
ms.locfileid: "93926362"
---
# <span data-ttu-id="e4829-101">Get-AzStorageSyncServerEndpoint</span><span class="sxs-lookup"><span data-stu-id="e4829-101">Get-AzStorageSyncServerEndpoint</span></span>

## <span data-ttu-id="e4829-102">Sammanfattning</span><span class="sxs-lookup"><span data-stu-id="e4829-102">SYNOPSIS</span></span>
<span data-ttu-id="e4829-103">Det här kommandot visar alla Server slut punkter i en given synkroniseringskoppling.</span><span class="sxs-lookup"><span data-stu-id="e4829-103">This command lists all server endpoints within a given sync group.</span></span>

## <span data-ttu-id="e4829-104">FRÅGESYNTAXEN</span><span class="sxs-lookup"><span data-stu-id="e4829-104">SYNTAX</span></span>

### <span data-ttu-id="e4829-105">StringParameterSet (standard)</span><span class="sxs-lookup"><span data-stu-id="e4829-105">StringParameterSet (Default)</span></span>
```
Get-AzStorageSyncServerEndpoint [-ResourceGroupName] <String> [-StorageSyncServiceName] <String>
 [-SyncGroupName] <String> [-Name <String>] [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="e4829-106">ObjectParameterSet</span><span class="sxs-lookup"><span data-stu-id="e4829-106">ObjectParameterSet</span></span>
```
Get-AzStorageSyncServerEndpoint [-ParentObject] <PSSyncGroup> [-Name <String>]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="e4829-107">ParentStringParameterSet</span><span class="sxs-lookup"><span data-stu-id="e4829-107">ParentStringParameterSet</span></span>
```
Get-AzStorageSyncServerEndpoint [-ParentResourceId] <String> [-Name <String>]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="e4829-108">PROBLEMBESKRIVNING</span><span class="sxs-lookup"><span data-stu-id="e4829-108">DESCRIPTION</span></span>
<span data-ttu-id="e4829-109">Det här kommandot visar alla Server slut punkter i en given synkroniseringskoppling.</span><span class="sxs-lookup"><span data-stu-id="e4829-109">This command lists all server endpoints within a given sync group.</span></span> <span data-ttu-id="e4829-110">Den kan också användas för att lista attributen för varje server slut punkt.</span><span class="sxs-lookup"><span data-stu-id="e4829-110">It can be used to also list the attributes of each server endpoint.</span></span>

## <span data-ttu-id="e4829-111">BESKRIVS</span><span class="sxs-lookup"><span data-stu-id="e4829-111">EXAMPLES</span></span>

### <span data-ttu-id="e4829-112">Exempel 1</span><span class="sxs-lookup"><span data-stu-id="e4829-112">Example 1</span></span>
```powershell
PS C:\> Get-AzStorageSyncServerEndpoint -ResourceGroupName "myResourceGroup" -StorageSyncServiceName "myStorageSyncServiceName" -SyncGroupName "mySyncGroupName"
```

<span data-ttu-id="e4829-113">Det här kommandot får alla Server slut punkter i den angivna synkroniseringsresursen.</span><span class="sxs-lookup"><span data-stu-id="e4829-113">This command gets all server endpoints contained within the specified sync group.</span></span> <span data-ttu-id="e4829-114">Ange-ServerEndpointName för att returnera ett specifikt nummer.</span><span class="sxs-lookup"><span data-stu-id="e4829-114">Specify -ServerEndpointName to return a specific one.</span></span>

## <span data-ttu-id="e4829-115">MALLPARAMETRAR</span><span class="sxs-lookup"><span data-stu-id="e4829-115">PARAMETERS</span></span>

### <span data-ttu-id="e4829-116">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="e4829-116">-DefaultProfile</span></span>
<span data-ttu-id="e4829-117">Autentiseringsuppgifter, konto, klient organisation och abonnemang som används för kommunikation med Azure.</span><span class="sxs-lookup"><span data-stu-id="e4829-117">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="e4829-118">-Namn</span><span class="sxs-lookup"><span data-stu-id="e4829-118">-Name</span></span>
<span data-ttu-id="e4829-119">Namnet på Server slut punkten.</span><span class="sxs-lookup"><span data-stu-id="e4829-119">Name of the server endpoint.</span></span>

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

### <span data-ttu-id="e4829-120">-ParentObject</span><span class="sxs-lookup"><span data-stu-id="e4829-120">-ParentObject</span></span>
<span data-ttu-id="e4829-121">StorageSyncService-objekt som normalt passerar genom parametern.</span><span class="sxs-lookup"><span data-stu-id="e4829-121">StorageSyncService Object, normally passed through the parameter.</span></span>

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

### <span data-ttu-id="e4829-122">-ParentResourceId</span><span class="sxs-lookup"><span data-stu-id="e4829-122">-ParentResourceId</span></span>
<span data-ttu-id="e4829-123">StorageSyncService-objekt som normalt passerar genom parametern.</span><span class="sxs-lookup"><span data-stu-id="e4829-123">StorageSyncService Object, normally passed through the parameter.</span></span>

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

### <span data-ttu-id="e4829-124">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="e4829-124">-ResourceGroupName</span></span>
<span data-ttu-id="e4829-125">Resurs grupps namn.</span><span class="sxs-lookup"><span data-stu-id="e4829-125">Resource Group Name.</span></span>

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

### <span data-ttu-id="e4829-126">-StorageSyncServiceName</span><span class="sxs-lookup"><span data-stu-id="e4829-126">-StorageSyncServiceName</span></span>
<span data-ttu-id="e4829-127">Namn på StorageSyncService.</span><span class="sxs-lookup"><span data-stu-id="e4829-127">Name of the StorageSyncService.</span></span>

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

### <span data-ttu-id="e4829-128">-SyncGroupName</span><span class="sxs-lookup"><span data-stu-id="e4829-128">-SyncGroupName</span></span>
<span data-ttu-id="e4829-129">Namn på SyncGroup.</span><span class="sxs-lookup"><span data-stu-id="e4829-129">Name of the SyncGroup.</span></span>

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

### <span data-ttu-id="e4829-130">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="e4829-130">CommonParameters</span></span>
<span data-ttu-id="e4829-131">Den här cmdleten har stöd för de gemensamma parametrarna:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-disvariable,-utbuffer,-PipelineVariable,-verbose,-WarningAction och-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="e4829-131">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="e4829-132">Mer information finns i about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="e4829-132">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="e4829-133">KOSTNADS</span><span class="sxs-lookup"><span data-stu-id="e4829-133">INPUTS</span></span>

### <span data-ttu-id="e4829-134">Microsoft. Azure. commands. StorageSync. Models. PSSyncGroup</span><span class="sxs-lookup"><span data-stu-id="e4829-134">Microsoft.Azure.Commands.StorageSync.Models.PSSyncGroup</span></span>

### <span data-ttu-id="e4829-135">System. String</span><span class="sxs-lookup"><span data-stu-id="e4829-135">System.String</span></span>

## <span data-ttu-id="e4829-136">VÄRDEN</span><span class="sxs-lookup"><span data-stu-id="e4829-136">OUTPUTS</span></span>

### <span data-ttu-id="e4829-137">Microsoft. Azure. commands. StorageSync. Models. PSServerEndpoint</span><span class="sxs-lookup"><span data-stu-id="e4829-137">Microsoft.Azure.Commands.StorageSync.Models.PSServerEndpoint</span></span>

## <span data-ttu-id="e4829-138">ANMÄRKNINGAR</span><span class="sxs-lookup"><span data-stu-id="e4829-138">NOTES</span></span>

## <span data-ttu-id="e4829-139">RELATERADE LÄNKAR</span><span class="sxs-lookup"><span data-stu-id="e4829-139">RELATED LINKS</span></span>
