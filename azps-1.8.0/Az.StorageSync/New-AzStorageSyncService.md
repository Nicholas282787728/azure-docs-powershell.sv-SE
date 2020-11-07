---
external help file: Microsoft.Azure.Commands.StorageSync.dll-Help.xml
Module Name: Az.StorageSync
online version: https://docs.microsoft.com/en-us/powershell/module/Az.storagesync/new-Azstoragesyncservice
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/StorageSync/StorageSync/help/New-AzStorageSyncService.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/StorageSync/StorageSync/help/New-AzStorageSyncService.md
ms.openlocfilehash: d2d18a908b53c9a8ab077671b7e2026516d40b17
ms.sourcegitcommit: 4d2c178cd6df9151877b08d54c1f4a228dbec9d1
ms.translationtype: MT
ms.contentlocale: sv-SE
ms.lasthandoff: 01/29/2020
ms.locfileid: "93746212"
---
# <span data-ttu-id="b4f37-101">New-AzStorageSyncService</span><span class="sxs-lookup"><span data-stu-id="b4f37-101">New-AzStorageSyncService</span></span>

## <span data-ttu-id="b4f37-102">Sammanfattning</span><span class="sxs-lookup"><span data-stu-id="b4f37-102">SYNOPSIS</span></span>
<span data-ttu-id="b4f37-103">Det här kommandot skapar en ny lagrings synkroniseringstjänst i en resurs grupp.</span><span class="sxs-lookup"><span data-stu-id="b4f37-103">This command creates a new storage sync service in a resource group.</span></span>

## <span data-ttu-id="b4f37-104">FRÅGESYNTAXEN</span><span class="sxs-lookup"><span data-stu-id="b4f37-104">SYNTAX</span></span>

```
New-AzStorageSyncService [-ResourceGroupName] <String> [-Name] <String> [-Location] <String>
 [[-Tag] <Hashtable>] [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="b4f37-105">PROBLEMBESKRIVNING</span><span class="sxs-lookup"><span data-stu-id="b4f37-105">DESCRIPTION</span></span>
<span data-ttu-id="b4f37-106">En synkroniseringstjänst för lagring är den högsta nivå resursen för Azure-filsynkronisering. Det här kommandot skapar en ny lagrings synkroniseringstjänst i en resurs grupp.</span><span class="sxs-lookup"><span data-stu-id="b4f37-106">A storage sync service is the top level resource for Azure File Sync. This command creates a new storage sync service in a resource group.</span></span> <span data-ttu-id="b4f37-107">Vi rekommenderar att du skapar så lite lagrings synctjänster som behövs för att skilja olika grupper av servrar i organisationen.</span><span class="sxs-lookup"><span data-stu-id="b4f37-107">We recommend to create as few storage sync services as absolutely necessary to differentiate distinct groups of servers in your organization.</span></span> <span data-ttu-id="b4f37-108">En synkroniseringstjänst för lagring innehåller Sync-grupper och fungerar också som ett mål för registrering av dina servrar.</span><span class="sxs-lookup"><span data-stu-id="b4f37-108">A storage sync service contains sync groups and also works as a target to register your servers to.</span></span> <span data-ttu-id="b4f37-109">En server kan bara vara registrerad på en enda lagrings synkroniseringstjänst.</span><span class="sxs-lookup"><span data-stu-id="b4f37-109">A server can only be registered to a single storage sync service.</span></span> <span data-ttu-id="b4f37-110">Om servrar någonsin behöver delta i synkroniseringen av samma uppsättning filer registrerar du dem på samma synkroniseringstjänst för lagring.</span><span class="sxs-lookup"><span data-stu-id="b4f37-110">If servers ever need to participate in syncing the same set of files, register them to the same storage sync service.</span></span>

## <span data-ttu-id="b4f37-111">BESKRIVS</span><span class="sxs-lookup"><span data-stu-id="b4f37-111">EXAMPLES</span></span>

### <span data-ttu-id="b4f37-112">Exempel 1</span><span class="sxs-lookup"><span data-stu-id="b4f37-112">Example 1</span></span>
```powershell
PS C:\> New-AzStorageSyncService -ResourceGroupName "myResourceGroup" -Location "myLocation" -StorageSyncServiceName "myStorageSyncServiceName"
```

<span data-ttu-id="b4f37-113">Det här kommandot skapar en synkroniseringstjänst för lagring.</span><span class="sxs-lookup"><span data-stu-id="b4f37-113">This command will create a storage sync service.</span></span>

## <span data-ttu-id="b4f37-114">MALLPARAMETRAR</span><span class="sxs-lookup"><span data-stu-id="b4f37-114">PARAMETERS</span></span>

### <span data-ttu-id="b4f37-115">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="b4f37-115">-DefaultProfile</span></span>
<span data-ttu-id="b4f37-116">Autentiseringsuppgifter, konto, klient organisation och abonnemang som används för kommunikation med Azure.</span><span class="sxs-lookup"><span data-stu-id="b4f37-116">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="b4f37-117">-Plats</span><span class="sxs-lookup"><span data-stu-id="b4f37-117">-Location</span></span>
<span data-ttu-id="b4f37-118">Plats för lagrings platsen.</span><span class="sxs-lookup"><span data-stu-id="b4f37-118">Storage Sync Service location.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: True
Position: 2
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="b4f37-119">-Namn</span><span class="sxs-lookup"><span data-stu-id="b4f37-119">-Name</span></span>
<span data-ttu-id="b4f37-120">Namn på Storage Sync-tjänsten.</span><span class="sxs-lookup"><span data-stu-id="b4f37-120">Name of the storage sync service.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases: StorageSyncServiceName

Required: True
Position: 1
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="b4f37-121">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="b4f37-121">-ResourceGroupName</span></span>
<span data-ttu-id="b4f37-122">Resurs grupps namn.</span><span class="sxs-lookup"><span data-stu-id="b4f37-122">Resource Group Name.</span></span>

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

### <span data-ttu-id="b4f37-123">-Tagg</span><span class="sxs-lookup"><span data-stu-id="b4f37-123">-Tag</span></span>
<span data-ttu-id="b4f37-124">Tjänst märkning för Storage Sync.</span><span class="sxs-lookup"><span data-stu-id="b4f37-124">Storage Sync Service Tags.</span></span>

```yaml
Type: System.Collections.Hashtable
Parameter Sets: (All)
Aliases: Tags

Required: False
Position: 3
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="b4f37-125">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="b4f37-125">CommonParameters</span></span>
<span data-ttu-id="b4f37-126">Den här cmdleten har stöd för de gemensamma parametrarna:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-disvariable,-utbuffer,-PipelineVariable,-verbose,-WarningAction och-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="b4f37-126">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="b4f37-127">Mer information finns i about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="b4f37-127">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="b4f37-128">KOSTNADS</span><span class="sxs-lookup"><span data-stu-id="b4f37-128">INPUTS</span></span>

### <span data-ttu-id="b4f37-129">System. String</span><span class="sxs-lookup"><span data-stu-id="b4f37-129">System.String</span></span>

## <span data-ttu-id="b4f37-130">VÄRDEN</span><span class="sxs-lookup"><span data-stu-id="b4f37-130">OUTPUTS</span></span>

### <span data-ttu-id="b4f37-131">Microsoft. Azure. commands. StorageSync. Models. PSStorageSyncService</span><span class="sxs-lookup"><span data-stu-id="b4f37-131">Microsoft.Azure.Commands.StorageSync.Models.PSStorageSyncService</span></span>

## <span data-ttu-id="b4f37-132">ANMÄRKNINGAR</span><span class="sxs-lookup"><span data-stu-id="b4f37-132">NOTES</span></span>

## <span data-ttu-id="b4f37-133">RELATERADE LÄNKAR</span><span class="sxs-lookup"><span data-stu-id="b4f37-133">RELATED LINKS</span></span>
