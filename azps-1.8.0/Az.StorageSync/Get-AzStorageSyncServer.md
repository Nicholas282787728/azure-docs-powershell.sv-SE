---
external help file: Microsoft.Azure.Commands.StorageSync.dll-Help.xml
Module Name: Az.StorageSync
online version: https://docs.microsoft.com/en-us/powershell/module/Az.storagesync/get-Azstoragesyncserver
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/StorageSync/StorageSync/help/Get-AzStorageSyncServer.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/StorageSync/StorageSync/help/Get-AzStorageSyncServer.md
ms.openlocfilehash: a9d5b5582a630a3131761d44c329a47c49546f11
ms.sourcegitcommit: 4d2c178cd6df9151877b08d54c1f4a228dbec9d1
ms.translationtype: MT
ms.contentlocale: sv-SE
ms.lasthandoff: 01/29/2020
ms.locfileid: "93746229"
---
# <span data-ttu-id="fabe4-101">Get-AzStorageSyncServer</span><span class="sxs-lookup"><span data-stu-id="fabe4-101">Get-AzStorageSyncServer</span></span>

## <span data-ttu-id="fabe4-102">Sammanfattning</span><span class="sxs-lookup"><span data-stu-id="fabe4-102">SYNOPSIS</span></span>
<span data-ttu-id="fabe4-103">Det här kommandot visar alla servrar registrerade till en given synkroniseringstjänst för lagring.</span><span class="sxs-lookup"><span data-stu-id="fabe4-103">This command lists all servers registered to a given storage sync service.</span></span>

## <span data-ttu-id="fabe4-104">FRÅGESYNTAXEN</span><span class="sxs-lookup"><span data-stu-id="fabe4-104">SYNTAX</span></span>

### <span data-ttu-id="fabe4-105">ObjectParameterSet (standard)</span><span class="sxs-lookup"><span data-stu-id="fabe4-105">ObjectParameterSet (Default)</span></span>
```
Get-AzStorageSyncServer [-ParentObject] <PSStorageSyncService> [-ServerId <Guid>]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="fabe4-106">StringParameterSet</span><span class="sxs-lookup"><span data-stu-id="fabe4-106">StringParameterSet</span></span>
```
Get-AzStorageSyncServer [-ResourceGroupName] <String> [-StorageSyncServiceName] <String> [-ServerId <Guid>]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="fabe4-107">ParentStringParameterSet</span><span class="sxs-lookup"><span data-stu-id="fabe4-107">ParentStringParameterSet</span></span>
```
Get-AzStorageSyncServer [-ParentResourceId] <String> [-ServerId <Guid>]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="fabe4-108">PROBLEMBESKRIVNING</span><span class="sxs-lookup"><span data-stu-id="fabe4-108">DESCRIPTION</span></span>
<span data-ttu-id="fabe4-109">Det här kommandot visar alla servrar registrerade till en given synkroniseringstjänst för lagring.</span><span class="sxs-lookup"><span data-stu-id="fabe4-109">This command lists all servers registered to a given storage sync service.</span></span> <span data-ttu-id="fabe4-110">Den kan även användas för att visa attributen för varje registrerad Server.</span><span class="sxs-lookup"><span data-stu-id="fabe4-110">It can be used to also list the attributes of each registered server.</span></span>

## <span data-ttu-id="fabe4-111">BESKRIVS</span><span class="sxs-lookup"><span data-stu-id="fabe4-111">EXAMPLES</span></span>

### <span data-ttu-id="fabe4-112">Exempel 1</span><span class="sxs-lookup"><span data-stu-id="fabe4-112">Example 1</span></span>
```powershell
PS C:\> Get-AzStorageSyncServer -ResourceGroupName "myResourceGroup" -StorageSyncServiceName "myStorageSyncServiceName"
```

<span data-ttu-id="fabe4-113">Med det här kommandot hämtas alla servrar registrerade till en specifik synkroniseringstjänst för lagring.</span><span class="sxs-lookup"><span data-stu-id="fabe4-113">This command gets all servers registered to a specific storage sync service.</span></span>

## <span data-ttu-id="fabe4-114">MALLPARAMETRAR</span><span class="sxs-lookup"><span data-stu-id="fabe4-114">PARAMETERS</span></span>

### <span data-ttu-id="fabe4-115">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="fabe4-115">-DefaultProfile</span></span>
<span data-ttu-id="fabe4-116">Autentiseringsuppgifter, konto, klient organisation och abonnemang som används för kommunikation med Azure.</span><span class="sxs-lookup"><span data-stu-id="fabe4-116">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="fabe4-117">-ParentObject</span><span class="sxs-lookup"><span data-stu-id="fabe4-117">-ParentObject</span></span>
<span data-ttu-id="fabe4-118">StorageSyncService-objekt som normalt passerar genom parametern.</span><span class="sxs-lookup"><span data-stu-id="fabe4-118">StorageSyncService Object, normally passed through the parameter.</span></span>

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

### <span data-ttu-id="fabe4-119">-ParentResourceId</span><span class="sxs-lookup"><span data-stu-id="fabe4-119">-ParentResourceId</span></span>
<span data-ttu-id="fabe4-120">StorageSyncService-objekt som normalt passerar genom parametern.</span><span class="sxs-lookup"><span data-stu-id="fabe4-120">StorageSyncService Object, normally passed through the parameter.</span></span>

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

### <span data-ttu-id="fabe4-121">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="fabe4-121">-ResourceGroupName</span></span>
<span data-ttu-id="fabe4-122">Resurs grupps namn.</span><span class="sxs-lookup"><span data-stu-id="fabe4-122">Resource Group Name.</span></span>

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

### <span data-ttu-id="fabe4-123">-ServerId</span><span class="sxs-lookup"><span data-stu-id="fabe4-123">-ServerId</span></span>
<span data-ttu-id="fabe4-124">Namn på RegisteredServer.</span><span class="sxs-lookup"><span data-stu-id="fabe4-124">Name of the RegisteredServer.</span></span>

```yaml
Type: System.Guid
Parameter Sets: (All)
Aliases: RegisteredServerName

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="fabe4-125">-StorageSyncServiceName</span><span class="sxs-lookup"><span data-stu-id="fabe4-125">-StorageSyncServiceName</span></span>
<span data-ttu-id="fabe4-126">Namn på StorageSyncService.</span><span class="sxs-lookup"><span data-stu-id="fabe4-126">Name of the StorageSyncService.</span></span>

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

### <span data-ttu-id="fabe4-127">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="fabe4-127">CommonParameters</span></span>
<span data-ttu-id="fabe4-128">Den här cmdleten har stöd för de gemensamma parametrarna:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-disvariable,-utbuffer,-PipelineVariable,-verbose,-WarningAction och-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="fabe4-128">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="fabe4-129">Mer information finns i about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="fabe4-129">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="fabe4-130">KOSTNADS</span><span class="sxs-lookup"><span data-stu-id="fabe4-130">INPUTS</span></span>

### <span data-ttu-id="fabe4-131">System. String</span><span class="sxs-lookup"><span data-stu-id="fabe4-131">System.String</span></span>

### <span data-ttu-id="fabe4-132">Microsoft. Azure. commands. StorageSync. Models. PSStorageSyncService</span><span class="sxs-lookup"><span data-stu-id="fabe4-132">Microsoft.Azure.Commands.StorageSync.Models.PSStorageSyncService</span></span>

### <span data-ttu-id="fabe4-133">System. GUID</span><span class="sxs-lookup"><span data-stu-id="fabe4-133">System.Guid</span></span>

## <span data-ttu-id="fabe4-134">VÄRDEN</span><span class="sxs-lookup"><span data-stu-id="fabe4-134">OUTPUTS</span></span>

### <span data-ttu-id="fabe4-135">Microsoft. Azure. commands. StorageSync. Models. PSRegisteredServer</span><span class="sxs-lookup"><span data-stu-id="fabe4-135">Microsoft.Azure.Commands.StorageSync.Models.PSRegisteredServer</span></span>

## <span data-ttu-id="fabe4-136">ANMÄRKNINGAR</span><span class="sxs-lookup"><span data-stu-id="fabe4-136">NOTES</span></span>

## <span data-ttu-id="fabe4-137">RELATERADE LÄNKAR</span><span class="sxs-lookup"><span data-stu-id="fabe4-137">RELATED LINKS</span></span>
