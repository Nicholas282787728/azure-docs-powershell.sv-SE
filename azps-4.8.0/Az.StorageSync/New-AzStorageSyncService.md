---
external help file: Microsoft.Azure.PowerShell.Cmdlets.StorageSync.dll-Help.xml
Module Name: Az.StorageSync
online version: https://docs.microsoft.com/en-us/powershell/module/Az.storagesync/new-Azstoragesyncservice
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/StorageSync/StorageSync/help/New-AzStorageSyncService.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/StorageSync/StorageSync/help/New-AzStorageSyncService.md
ms.openlocfilehash: 0476a881ec1ee479b97dad4ab8dcf95121dd5302
ms.sourcegitcommit: 1de2b6c3c99197958fa2101bc37680e7507f91ac
ms.translationtype: MT
ms.contentlocale: sv-SE
ms.lasthandoff: 10/13/2020
ms.locfileid: "94258983"
---
# <span data-ttu-id="09fd8-101">New-AzStorageSyncService</span><span class="sxs-lookup"><span data-stu-id="09fd8-101">New-AzStorageSyncService</span></span>

## <span data-ttu-id="09fd8-102">Sammanfattning</span><span class="sxs-lookup"><span data-stu-id="09fd8-102">SYNOPSIS</span></span>
<span data-ttu-id="09fd8-103">Det här kommandot skapar en ny lagrings synkroniseringstjänst i en resurs grupp.</span><span class="sxs-lookup"><span data-stu-id="09fd8-103">This command creates a new storage sync service in a resource group.</span></span>

## <span data-ttu-id="09fd8-104">FRÅGESYNTAXEN</span><span class="sxs-lookup"><span data-stu-id="09fd8-104">SYNTAX</span></span>

```
New-AzStorageSyncService [-ResourceGroupName] <String> [-Name] <String> [-Location] <String> [-IncomingTrafficPolicy] <String> [-Tag <Hashtable>]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="09fd8-105">PROBLEMBESKRIVNING</span><span class="sxs-lookup"><span data-stu-id="09fd8-105">DESCRIPTION</span></span>
<span data-ttu-id="09fd8-106">En synkroniseringstjänst för lagring är den högsta nivå resursen för Azure-filsynkronisering. Det här kommandot skapar en ny lagrings synkroniseringstjänst i en resurs grupp.</span><span class="sxs-lookup"><span data-stu-id="09fd8-106">A storage sync service is the top level resource for Azure File Sync. This command creates a new storage sync service in a resource group.</span></span> <span data-ttu-id="09fd8-107">Vi rekommenderar att du skapar så lite lagrings synctjänster som behövs för att skilja olika grupper av servrar i organisationen.</span><span class="sxs-lookup"><span data-stu-id="09fd8-107">We recommend to create as few storage sync services as absolutely necessary to differentiate distinct groups of servers in your organization.</span></span> <span data-ttu-id="09fd8-108">En synkroniseringstjänst för lagring innehåller Sync-grupper och fungerar också som ett mål för registrering av dina servrar.</span><span class="sxs-lookup"><span data-stu-id="09fd8-108">A storage sync service contains sync groups and also works as a target to register your servers to.</span></span> <span data-ttu-id="09fd8-109">En server kan bara vara registrerad på en enda lagrings synkroniseringstjänst.</span><span class="sxs-lookup"><span data-stu-id="09fd8-109">A server can only be registered to a single storage sync service.</span></span> <span data-ttu-id="09fd8-110">Om servrar någonsin behöver delta i synkroniseringen av samma uppsättning filer registrerar du dem på samma synkroniseringstjänst för lagring.</span><span class="sxs-lookup"><span data-stu-id="09fd8-110">If servers ever need to participate in syncing the same set of files, register them to the same storage sync service.</span></span>

## <span data-ttu-id="09fd8-111">BESKRIVS</span><span class="sxs-lookup"><span data-stu-id="09fd8-111">EXAMPLES</span></span>

### <span data-ttu-id="09fd8-112">Exempel 1</span><span class="sxs-lookup"><span data-stu-id="09fd8-112">Example 1</span></span>
```powershell
PS C:\> New-AzStorageSyncService -ResourceGroupName "myResourceGroup" -Location "myLocation" -StorageSyncServiceName "myStorageSyncServiceName" -IncomingTrafficPolicy "AllowAllTraffic"
```

<span data-ttu-id="09fd8-113">Det här kommandot skapar en synkroniseringstjänst för lagring.</span><span class="sxs-lookup"><span data-stu-id="09fd8-113">This command will create a storage sync service.</span></span>

## <span data-ttu-id="09fd8-114">MALLPARAMETRAR</span><span class="sxs-lookup"><span data-stu-id="09fd8-114">PARAMETERS</span></span>

### <span data-ttu-id="09fd8-115">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="09fd8-115">-DefaultProfile</span></span>
<span data-ttu-id="09fd8-116">Autentiseringsuppgifter, konto, klient organisation och abonnemang som används för kommunikation med Azure.</span><span class="sxs-lookup"><span data-stu-id="09fd8-116">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="09fd8-117">-Plats</span><span class="sxs-lookup"><span data-stu-id="09fd8-117">-Location</span></span>
<span data-ttu-id="09fd8-118">Plats för lagrings platsen.</span><span class="sxs-lookup"><span data-stu-id="09fd8-118">Storage Sync Service location.</span></span>

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

### <span data-ttu-id="09fd8-119">-IncomingTrafficPolicy</span><span class="sxs-lookup"><span data-stu-id="09fd8-119">-IncomingTrafficPolicy</span></span>
<span data-ttu-id="09fd8-120">IncomingTrafficPolicy för Storage Sync-tjänsten</span><span class="sxs-lookup"><span data-stu-id="09fd8-120">Storage Sync Service IncomingTrafficPolicy</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: True
Position: 3
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="09fd8-121">-Namn</span><span class="sxs-lookup"><span data-stu-id="09fd8-121">-Name</span></span>
<span data-ttu-id="09fd8-122">Namn på Storage Sync-tjänsten.</span><span class="sxs-lookup"><span data-stu-id="09fd8-122">Name of the storage sync service.</span></span>

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

### <span data-ttu-id="09fd8-123">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="09fd8-123">-ResourceGroupName</span></span>
<span data-ttu-id="09fd8-124">Resurs grupps namn.</span><span class="sxs-lookup"><span data-stu-id="09fd8-124">Resource Group Name.</span></span>

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

### <span data-ttu-id="09fd8-125">-Tagg</span><span class="sxs-lookup"><span data-stu-id="09fd8-125">-Tag</span></span>
<span data-ttu-id="09fd8-126">Tjänst märkning för Storage Sync.</span><span class="sxs-lookup"><span data-stu-id="09fd8-126">Storage Sync Service Tags.</span></span>

```yaml
Type: System.Collections.Hashtable
Parameter Sets: (All)
Aliases: Tags

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="09fd8-127">-Bekräfta</span><span class="sxs-lookup"><span data-stu-id="09fd8-127">-Confirm</span></span>
<span data-ttu-id="09fd8-128">Du uppmanas att bekräfta innan du kör cmdleten.</span><span class="sxs-lookup"><span data-stu-id="09fd8-128">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="09fd8-129">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="09fd8-129">-WhatIf</span></span>
<span data-ttu-id="09fd8-130">Visar vad som händer om cmdleten körs.</span><span class="sxs-lookup"><span data-stu-id="09fd8-130">Shows what would happen if the cmdlet runs.</span></span> <span data-ttu-id="09fd8-131">Cmdleten körs inte.</span><span class="sxs-lookup"><span data-stu-id="09fd8-131">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="09fd8-132">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="09fd8-132">CommonParameters</span></span>
<span data-ttu-id="09fd8-133">Den här cmdleten har stöd för de gemensamma parametrarna:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-disvariable,-utbuffer,-PipelineVariable,-verbose,-WarningAction och-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="09fd8-133">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="09fd8-134">Mer information finns i about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="09fd8-134">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="09fd8-135">KOSTNADS</span><span class="sxs-lookup"><span data-stu-id="09fd8-135">INPUTS</span></span>

### <span data-ttu-id="09fd8-136">System. String</span><span class="sxs-lookup"><span data-stu-id="09fd8-136">System.String</span></span>

## <span data-ttu-id="09fd8-137">VÄRDEN</span><span class="sxs-lookup"><span data-stu-id="09fd8-137">OUTPUTS</span></span>

### <span data-ttu-id="09fd8-138">Microsoft. Azure. commands. StorageSync. Models. PSStorageSyncService</span><span class="sxs-lookup"><span data-stu-id="09fd8-138">Microsoft.Azure.Commands.StorageSync.Models.PSStorageSyncService</span></span>

## <span data-ttu-id="09fd8-139">ANMÄRKNINGAR</span><span class="sxs-lookup"><span data-stu-id="09fd8-139">NOTES</span></span>

## <span data-ttu-id="09fd8-140">RELATERADE LÄNKAR</span><span class="sxs-lookup"><span data-stu-id="09fd8-140">RELATED LINKS</span></span>
