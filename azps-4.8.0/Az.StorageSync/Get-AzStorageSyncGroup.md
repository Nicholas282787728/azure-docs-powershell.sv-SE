---
external help file: Microsoft.Azure.PowerShell.Cmdlets.StorageSync.dll-Help.xml
Module Name: Az.StorageSync
online version: https://docs.microsoft.com/en-us/powershell/module/Az.storagesync/get-Azstoragesyncgroup
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/StorageSync/StorageSync/help/Get-AzStorageSyncGroup.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/StorageSync/StorageSync/help/Get-AzStorageSyncGroup.md
ms.openlocfilehash: b59d5dd1ca094d4b4d5eed276957f07b7d34f1f2
ms.sourcegitcommit: 1de2b6c3c99197958fa2101bc37680e7507f91ac
ms.translationtype: MT
ms.contentlocale: sv-SE
ms.lasthandoff: 10/13/2020
ms.locfileid: "94258471"
---
# <span data-ttu-id="9e49e-101">Get-AzStorageSyncGroup</span><span class="sxs-lookup"><span data-stu-id="9e49e-101">Get-AzStorageSyncGroup</span></span>

## <span data-ttu-id="9e49e-102">Sammanfattning</span><span class="sxs-lookup"><span data-stu-id="9e49e-102">SYNOPSIS</span></span>
<span data-ttu-id="9e49e-103">Det här kommandot visar alla synkroniseringsresurser i en given synkroniseringstjänst för lagring.</span><span class="sxs-lookup"><span data-stu-id="9e49e-103">This command lists all sync groups within a given storage sync service.</span></span>

## <span data-ttu-id="9e49e-104">FRÅGESYNTAXEN</span><span class="sxs-lookup"><span data-stu-id="9e49e-104">SYNTAX</span></span>

### <span data-ttu-id="9e49e-105">StringParameterSet (standard)</span><span class="sxs-lookup"><span data-stu-id="9e49e-105">StringParameterSet (Default)</span></span>
```
Get-AzStorageSyncGroup [-ResourceGroupName] <String> [-StorageSyncServiceName] <String> [-Name <String>]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="9e49e-106">ObjectParameterSet</span><span class="sxs-lookup"><span data-stu-id="9e49e-106">ObjectParameterSet</span></span>
```
Get-AzStorageSyncGroup [-ParentObject] <PSStorageSyncService> [-Name <String>]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="9e49e-107">ParentStringParameterSet</span><span class="sxs-lookup"><span data-stu-id="9e49e-107">ParentStringParameterSet</span></span>
```
Get-AzStorageSyncGroup [-ParentResourceId] <String> [-Name <String>] [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

## <span data-ttu-id="9e49e-108">PROBLEMBESKRIVNING</span><span class="sxs-lookup"><span data-stu-id="9e49e-108">DESCRIPTION</span></span>
<span data-ttu-id="9e49e-109">Det här kommandot visar alla synkroniseringsresurser i en given synkroniseringstjänst för lagring.</span><span class="sxs-lookup"><span data-stu-id="9e49e-109">This command lists all sync groups within a given storage sync service.</span></span> <span data-ttu-id="9e49e-110">Den kan också användas för att lista attributen för varje synkroniseringsresurs.</span><span class="sxs-lookup"><span data-stu-id="9e49e-110">It can be used to also list the attributes of each sync group.</span></span>

## <span data-ttu-id="9e49e-111">BESKRIVS</span><span class="sxs-lookup"><span data-stu-id="9e49e-111">EXAMPLES</span></span>

### <span data-ttu-id="9e49e-112">Exempel 1</span><span class="sxs-lookup"><span data-stu-id="9e49e-112">Example 1</span></span>
```powershell
PS C:\> Get-AzStorageSyncGroup New-AzStorageSyncCloudEndpoint -ResourceGroupName "myResourceGroup" -StorageSyncServiceName "myStorageSyncServiceName"
```

<span data-ttu-id="9e49e-113">Det här kommandot får alla synkroniserade grupper i den angivna tjänsten för lagrings synkronisering.</span><span class="sxs-lookup"><span data-stu-id="9e49e-113">This command gets all sync groups contained within the specified storage sync service.</span></span> <span data-ttu-id="9e49e-114">Ange-namn för att returnera en viss.</span><span class="sxs-lookup"><span data-stu-id="9e49e-114">Specify -Name to return a specific one.</span></span>

## <span data-ttu-id="9e49e-115">MALLPARAMETRAR</span><span class="sxs-lookup"><span data-stu-id="9e49e-115">PARAMETERS</span></span>

### <span data-ttu-id="9e49e-116">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="9e49e-116">-DefaultProfile</span></span>
<span data-ttu-id="9e49e-117">Autentiseringsuppgifter, konto, klient organisation och abonnemang som används för kommunikation med Azure.</span><span class="sxs-lookup"><span data-stu-id="9e49e-117">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="9e49e-118">-Namn</span><span class="sxs-lookup"><span data-stu-id="9e49e-118">-Name</span></span>
<span data-ttu-id="9e49e-119">Namn på SyncGroup.</span><span class="sxs-lookup"><span data-stu-id="9e49e-119">Name of the SyncGroup.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases: SyncGroupName

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="9e49e-120">-ParentObject</span><span class="sxs-lookup"><span data-stu-id="9e49e-120">-ParentObject</span></span>
<span data-ttu-id="9e49e-121">StorageSyncService-objekt som normalt passerar genom parametern.</span><span class="sxs-lookup"><span data-stu-id="9e49e-121">StorageSyncService Object, normally passed through the parameter.</span></span>

```yaml
Type: Microsoft.Azure.Commands.StorageSync.Models.PSStorageSyncService
Parameter Sets: ObjectParameterSet
Aliases: StorageSyncService

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="9e49e-122">-ParentResourceId</span><span class="sxs-lookup"><span data-stu-id="9e49e-122">-ParentResourceId</span></span>
<span data-ttu-id="9e49e-123">StorageSyncService-objekt som normalt passerar genom parametern.</span><span class="sxs-lookup"><span data-stu-id="9e49e-123">StorageSyncService Object, normally passed through the parameter.</span></span>

```yaml
Type: System.String
Parameter Sets: ParentStringParameterSet
Aliases: StorageSyncServiceId

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="9e49e-124">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="9e49e-124">-ResourceGroupName</span></span>
<span data-ttu-id="9e49e-125">Resurs grupps namn.</span><span class="sxs-lookup"><span data-stu-id="9e49e-125">Resource Group Name.</span></span>

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

### <span data-ttu-id="9e49e-126">-StorageSyncServiceName</span><span class="sxs-lookup"><span data-stu-id="9e49e-126">-StorageSyncServiceName</span></span>
<span data-ttu-id="9e49e-127">Namn på StorageSyncService.</span><span class="sxs-lookup"><span data-stu-id="9e49e-127">Name of the StorageSyncService.</span></span>

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

### <span data-ttu-id="9e49e-128">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="9e49e-128">CommonParameters</span></span>
<span data-ttu-id="9e49e-129">Den här cmdleten har stöd för de gemensamma parametrarna:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-disvariable,-utbuffer,-PipelineVariable,-verbose,-WarningAction och-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="9e49e-129">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="9e49e-130">Mer information finns i about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="9e49e-130">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="9e49e-131">KOSTNADS</span><span class="sxs-lookup"><span data-stu-id="9e49e-131">INPUTS</span></span>

### <span data-ttu-id="9e49e-132">System. String</span><span class="sxs-lookup"><span data-stu-id="9e49e-132">System.String</span></span>

### <span data-ttu-id="9e49e-133">Microsoft. Azure. commands. StorageSync. Models. PSStorageSyncService</span><span class="sxs-lookup"><span data-stu-id="9e49e-133">Microsoft.Azure.Commands.StorageSync.Models.PSStorageSyncService</span></span>

## <span data-ttu-id="9e49e-134">VÄRDEN</span><span class="sxs-lookup"><span data-stu-id="9e49e-134">OUTPUTS</span></span>

### <span data-ttu-id="9e49e-135">Microsoft. Azure. commands. StorageSync. Models. PSSyncGroup</span><span class="sxs-lookup"><span data-stu-id="9e49e-135">Microsoft.Azure.Commands.StorageSync.Models.PSSyncGroup</span></span>

## <span data-ttu-id="9e49e-136">ANMÄRKNINGAR</span><span class="sxs-lookup"><span data-stu-id="9e49e-136">NOTES</span></span>

## <span data-ttu-id="9e49e-137">RELATERADE LÄNKAR</span><span class="sxs-lookup"><span data-stu-id="9e49e-137">RELATED LINKS</span></span>
