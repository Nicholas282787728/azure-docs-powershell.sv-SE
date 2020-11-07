---
external help file: Microsoft.Azure.PowerShell.Cmdlets.StorageSync.dll-Help.xml
Module Name: Az.StorageSync
online version: https://docs.microsoft.com/en-us/powershell/module/Az.storagesync/get-Azstoragesyncserver
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/StorageSync/StorageSync/help/Get-AzStorageSyncServer.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/StorageSync/StorageSync/help/Get-AzStorageSyncServer.md
ms.openlocfilehash: ebee7b772fc4da3ef14d2273b79b089d57fa317f
ms.sourcegitcommit: 6a91b4c545350d316d3cf8c62f384478e3f3ba24
ms.translationtype: MT
ms.contentlocale: sv-SE
ms.lasthandoff: 04/21/2020
ms.locfileid: "93927317"
---
# <span data-ttu-id="77cd8-101">Get-AzStorageSyncServer</span><span class="sxs-lookup"><span data-stu-id="77cd8-101">Get-AzStorageSyncServer</span></span>

## <span data-ttu-id="77cd8-102">Sammanfattning</span><span class="sxs-lookup"><span data-stu-id="77cd8-102">SYNOPSIS</span></span>
<span data-ttu-id="77cd8-103">Det här kommandot visar alla servrar registrerade till en given synkroniseringstjänst för lagring.</span><span class="sxs-lookup"><span data-stu-id="77cd8-103">This command lists all servers registered to a given storage sync service.</span></span>

## <span data-ttu-id="77cd8-104">FRÅGESYNTAXEN</span><span class="sxs-lookup"><span data-stu-id="77cd8-104">SYNTAX</span></span>

### <span data-ttu-id="77cd8-105">StringParameterSet (standard)</span><span class="sxs-lookup"><span data-stu-id="77cd8-105">StringParameterSet (Default)</span></span>
```
Get-AzStorageSyncServer [-ResourceGroupName] <String> [-StorageSyncServiceName] <String> [-ServerId <Guid>]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="77cd8-106">ObjectParameterSet</span><span class="sxs-lookup"><span data-stu-id="77cd8-106">ObjectParameterSet</span></span>
```
Get-AzStorageSyncServer [-ParentObject] <PSStorageSyncService> [-ServerId <Guid>]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="77cd8-107">ParentStringParameterSet</span><span class="sxs-lookup"><span data-stu-id="77cd8-107">ParentStringParameterSet</span></span>
```
Get-AzStorageSyncServer [-ParentResourceId] <String> [-ServerId <Guid>]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="77cd8-108">PROBLEMBESKRIVNING</span><span class="sxs-lookup"><span data-stu-id="77cd8-108">DESCRIPTION</span></span>
<span data-ttu-id="77cd8-109">Det här kommandot visar alla servrar registrerade till en given synkroniseringstjänst för lagring.</span><span class="sxs-lookup"><span data-stu-id="77cd8-109">This command lists all servers registered to a given storage sync service.</span></span> <span data-ttu-id="77cd8-110">Den kan även användas för att visa attributen för varje registrerad Server.</span><span class="sxs-lookup"><span data-stu-id="77cd8-110">It can be used to also list the attributes of each registered server.</span></span>

## <span data-ttu-id="77cd8-111">BESKRIVS</span><span class="sxs-lookup"><span data-stu-id="77cd8-111">EXAMPLES</span></span>

### <span data-ttu-id="77cd8-112">Exempel 1</span><span class="sxs-lookup"><span data-stu-id="77cd8-112">Example 1</span></span>
```powershell
PS C:\> Get-AzStorageSyncServer -ResourceGroupName "myResourceGroup" -StorageSyncServiceName "myStorageSyncServiceName"
```

<span data-ttu-id="77cd8-113">Med det här kommandot hämtas alla servrar registrerade till en specifik synkroniseringstjänst för lagring.</span><span class="sxs-lookup"><span data-stu-id="77cd8-113">This command gets all servers registered to a specific storage sync service.</span></span>

## <span data-ttu-id="77cd8-114">MALLPARAMETRAR</span><span class="sxs-lookup"><span data-stu-id="77cd8-114">PARAMETERS</span></span>

### <span data-ttu-id="77cd8-115">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="77cd8-115">-DefaultProfile</span></span>
<span data-ttu-id="77cd8-116">Autentiseringsuppgifter, konto, klient organisation och abonnemang som används för kommunikation med Azure.</span><span class="sxs-lookup"><span data-stu-id="77cd8-116">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="77cd8-117">-ParentObject</span><span class="sxs-lookup"><span data-stu-id="77cd8-117">-ParentObject</span></span>
<span data-ttu-id="77cd8-118">StorageSyncService-objekt som normalt passerar genom parametern.</span><span class="sxs-lookup"><span data-stu-id="77cd8-118">StorageSyncService Object, normally passed through the parameter.</span></span>

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

### <span data-ttu-id="77cd8-119">-ParentResourceId</span><span class="sxs-lookup"><span data-stu-id="77cd8-119">-ParentResourceId</span></span>
<span data-ttu-id="77cd8-120">StorageSyncService-objekt som normalt passerar genom parametern.</span><span class="sxs-lookup"><span data-stu-id="77cd8-120">StorageSyncService Object, normally passed through the parameter.</span></span>

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

### <span data-ttu-id="77cd8-121">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="77cd8-121">-ResourceGroupName</span></span>
<span data-ttu-id="77cd8-122">Resurs grupps namn.</span><span class="sxs-lookup"><span data-stu-id="77cd8-122">Resource Group Name.</span></span>

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

### <span data-ttu-id="77cd8-123">-ServerId</span><span class="sxs-lookup"><span data-stu-id="77cd8-123">-ServerId</span></span>
<span data-ttu-id="77cd8-124">Namn på RegisteredServer.</span><span class="sxs-lookup"><span data-stu-id="77cd8-124">Name of the RegisteredServer.</span></span>

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

### <span data-ttu-id="77cd8-125">-StorageSyncServiceName</span><span class="sxs-lookup"><span data-stu-id="77cd8-125">-StorageSyncServiceName</span></span>
<span data-ttu-id="77cd8-126">Namn på StorageSyncService.</span><span class="sxs-lookup"><span data-stu-id="77cd8-126">Name of the StorageSyncService.</span></span>

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

### <span data-ttu-id="77cd8-127">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="77cd8-127">CommonParameters</span></span>
<span data-ttu-id="77cd8-128">Den här cmdleten har stöd för de gemensamma parametrarna:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-disvariable,-utbuffer,-PipelineVariable,-verbose,-WarningAction och-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="77cd8-128">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="77cd8-129">Mer information finns i about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="77cd8-129">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="77cd8-130">KOSTNADS</span><span class="sxs-lookup"><span data-stu-id="77cd8-130">INPUTS</span></span>

### <span data-ttu-id="77cd8-131">System. String</span><span class="sxs-lookup"><span data-stu-id="77cd8-131">System.String</span></span>

### <span data-ttu-id="77cd8-132">Microsoft. Azure. commands. StorageSync. Models. PSStorageSyncService</span><span class="sxs-lookup"><span data-stu-id="77cd8-132">Microsoft.Azure.Commands.StorageSync.Models.PSStorageSyncService</span></span>

### <span data-ttu-id="77cd8-133">System. GUID</span><span class="sxs-lookup"><span data-stu-id="77cd8-133">System.Guid</span></span>

## <span data-ttu-id="77cd8-134">VÄRDEN</span><span class="sxs-lookup"><span data-stu-id="77cd8-134">OUTPUTS</span></span>

### <span data-ttu-id="77cd8-135">Microsoft. Azure. commands. StorageSync. Models. PSRegisteredServer</span><span class="sxs-lookup"><span data-stu-id="77cd8-135">Microsoft.Azure.Commands.StorageSync.Models.PSRegisteredServer</span></span>

## <span data-ttu-id="77cd8-136">ANMÄRKNINGAR</span><span class="sxs-lookup"><span data-stu-id="77cd8-136">NOTES</span></span>

## <span data-ttu-id="77cd8-137">RELATERADE LÄNKAR</span><span class="sxs-lookup"><span data-stu-id="77cd8-137">RELATED LINKS</span></span>
