---
external help file: Microsoft.Azure.Commands.StorageSync.dll-Help.xml
Module Name: Az.StorageSync
online version: https://docs.microsoft.com/en-us/powershell/module/Az.storagesync/new-Azstoragesyncgroup
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/StorageSync/StorageSync/help/New-AzStorageSyncGroup.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/StorageSync/StorageSync/help/New-AzStorageSyncGroup.md
ms.openlocfilehash: 34f4dc1933e755167333d12d4566838ea47c26b1
ms.sourcegitcommit: 4d2c178cd6df9151877b08d54c1f4a228dbec9d1
ms.translationtype: MT
ms.contentlocale: sv-SE
ms.lasthandoff: 01/29/2020
ms.locfileid: "93746214"
---
# <span data-ttu-id="8deb8-101">New-AzStorageSyncGroup</span><span class="sxs-lookup"><span data-stu-id="8deb8-101">New-AzStorageSyncGroup</span></span>

## <span data-ttu-id="8deb8-102">Sammanfattning</span><span class="sxs-lookup"><span data-stu-id="8deb8-102">SYNOPSIS</span></span>
<span data-ttu-id="8deb8-103">Det här kommandot skapar en ny synkroniseringsresurs i en angiven synkroniseringstjänst.</span><span class="sxs-lookup"><span data-stu-id="8deb8-103">This command creates a new sync group within a specified storage sync service.</span></span>

## <span data-ttu-id="8deb8-104">FRÅGESYNTAXEN</span><span class="sxs-lookup"><span data-stu-id="8deb8-104">SYNTAX</span></span>

### <span data-ttu-id="8deb8-105">ObjectParameterSet (standard)</span><span class="sxs-lookup"><span data-stu-id="8deb8-105">ObjectParameterSet (Default)</span></span>
```
New-AzStorageSyncGroup [-ParentObject] <PSStorageSyncService> -Name <String>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="8deb8-106">StringParameterSet</span><span class="sxs-lookup"><span data-stu-id="8deb8-106">StringParameterSet</span></span>
```
New-AzStorageSyncGroup [-ResourceGroupName] <String> [-StorageSyncServiceName] <String> -Name <String>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="8deb8-107">ParentStringParameterSet</span><span class="sxs-lookup"><span data-stu-id="8deb8-107">ParentStringParameterSet</span></span>
```
New-AzStorageSyncGroup [-ParentResourceId] <String> -Name <String> [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

## <span data-ttu-id="8deb8-108">PROBLEMBESKRIVNING</span><span class="sxs-lookup"><span data-stu-id="8deb8-108">DESCRIPTION</span></span>
<span data-ttu-id="8deb8-109">Det här kommandot skapar en ny synkroniseringsresurs i en angiven synkroniseringstjänst.</span><span class="sxs-lookup"><span data-stu-id="8deb8-109">This command creates a new sync group within a specified storage sync service.</span></span> <span data-ttu-id="8deb8-110">En synkroniseringsresurs används för att beskriva en topologi med platser som kallas slut punkter, som synkroniserar alla filer som lagras i en av slut punkterna.</span><span class="sxs-lookup"><span data-stu-id="8deb8-110">A sync group is used to describe a topology of locations, referred to as endpoints, that will sync any files stored within any one of the endpoints.</span></span> <span data-ttu-id="8deb8-111">En synkroniseringsresurs innehåller moln slut punkter som refererar till Azure-fildelningar och innehåller också Server slut punkter som refererar till en viss lokal sökväg på en registrerad Server.</span><span class="sxs-lookup"><span data-stu-id="8deb8-111">A sync group contains cloud endpoints, which reference Azure file shares, and it also contains server endpoints which reference a specific local path on a registered server.</span></span>

## <span data-ttu-id="8deb8-112">BESKRIVS</span><span class="sxs-lookup"><span data-stu-id="8deb8-112">EXAMPLES</span></span>

### <span data-ttu-id="8deb8-113">Exempel 1</span><span class="sxs-lookup"><span data-stu-id="8deb8-113">Example 1</span></span>
```powershell
PS C:\> New-AzStorageSyncGroup -ResourceGroupName "myResourceGroup" -StorageSyncServiceName "myStorageSyncServiceName" -Name "mySyncGroupName"
```

<span data-ttu-id="8deb8-114">Det här kommandot skapar en ny synkroniseringsresurs i en angiven synkroniseringstjänst.</span><span class="sxs-lookup"><span data-stu-id="8deb8-114">This command creates a new sync group within a specified storage sync service.</span></span>

## <span data-ttu-id="8deb8-115">MALLPARAMETRAR</span><span class="sxs-lookup"><span data-stu-id="8deb8-115">PARAMETERS</span></span>

### <span data-ttu-id="8deb8-116">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="8deb8-116">-DefaultProfile</span></span>
<span data-ttu-id="8deb8-117">Autentiseringsuppgifter, konto, klient organisation och abonnemang som används för kommunikation med Azure.</span><span class="sxs-lookup"><span data-stu-id="8deb8-117">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="8deb8-118">-Namn</span><span class="sxs-lookup"><span data-stu-id="8deb8-118">-Name</span></span>
<span data-ttu-id="8deb8-119">Namn på SyncGroup.</span><span class="sxs-lookup"><span data-stu-id="8deb8-119">Name of the SyncGroup.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases: SyncGroupName

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="8deb8-120">-ParentObject</span><span class="sxs-lookup"><span data-stu-id="8deb8-120">-ParentObject</span></span>
<span data-ttu-id="8deb8-121">StorageSyncService-objekt som normalt passerar genom parametern.</span><span class="sxs-lookup"><span data-stu-id="8deb8-121">StorageSyncService Object, normally passed through the parameter.</span></span>

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

### <span data-ttu-id="8deb8-122">-ParentResourceId</span><span class="sxs-lookup"><span data-stu-id="8deb8-122">-ParentResourceId</span></span>
<span data-ttu-id="8deb8-123">Överordnat resurs-ID för StorageSyncService</span><span class="sxs-lookup"><span data-stu-id="8deb8-123">StorageSyncService Parent Resource Id</span></span>

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

### <span data-ttu-id="8deb8-124">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="8deb8-124">-ResourceGroupName</span></span>
<span data-ttu-id="8deb8-125">Resurs grupps namn.</span><span class="sxs-lookup"><span data-stu-id="8deb8-125">Resource Group Name.</span></span>

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

### <span data-ttu-id="8deb8-126">-StorageSyncServiceName</span><span class="sxs-lookup"><span data-stu-id="8deb8-126">-StorageSyncServiceName</span></span>
<span data-ttu-id="8deb8-127">Namn på StorageSyncService.</span><span class="sxs-lookup"><span data-stu-id="8deb8-127">Name of the StorageSyncService.</span></span>

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

### <span data-ttu-id="8deb8-128">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="8deb8-128">CommonParameters</span></span>
<span data-ttu-id="8deb8-129">Den här cmdleten har stöd för de gemensamma parametrarna:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-disvariable,-utbuffer,-PipelineVariable,-verbose,-WarningAction och-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="8deb8-129">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="8deb8-130">Mer information finns i about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="8deb8-130">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="8deb8-131">KOSTNADS</span><span class="sxs-lookup"><span data-stu-id="8deb8-131">INPUTS</span></span>

### <span data-ttu-id="8deb8-132">System. String</span><span class="sxs-lookup"><span data-stu-id="8deb8-132">System.String</span></span>

### <span data-ttu-id="8deb8-133">Microsoft. Azure. commands. StorageSync. Models. PSStorageSyncService</span><span class="sxs-lookup"><span data-stu-id="8deb8-133">Microsoft.Azure.Commands.StorageSync.Models.PSStorageSyncService</span></span>

## <span data-ttu-id="8deb8-134">VÄRDEN</span><span class="sxs-lookup"><span data-stu-id="8deb8-134">OUTPUTS</span></span>

### <span data-ttu-id="8deb8-135">Microsoft. Azure. commands. StorageSync. Models. PSSyncGroup</span><span class="sxs-lookup"><span data-stu-id="8deb8-135">Microsoft.Azure.Commands.StorageSync.Models.PSSyncGroup</span></span>

## <span data-ttu-id="8deb8-136">ANMÄRKNINGAR</span><span class="sxs-lookup"><span data-stu-id="8deb8-136">NOTES</span></span>

## <span data-ttu-id="8deb8-137">RELATERADE LÄNKAR</span><span class="sxs-lookup"><span data-stu-id="8deb8-137">RELATED LINKS</span></span>
