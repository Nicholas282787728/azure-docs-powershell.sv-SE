---
external help file: Microsoft.Azure.PowerShell.Cmdlets.StorageSync.dll-Help.xml
Module Name: Az.StorageSync
online version: https://docs.microsoft.com/en-us/powershell/module/Az.storagesync/new-Azstoragesyncservice
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/StorageSync/StorageSync/help/New-AzStorageSyncService.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/StorageSync/StorageSync/help/New-AzStorageSyncService.md
ms.openlocfilehash: 0476a881ec1ee479b97dad4ab8dcf95121dd5302
ms.sourcegitcommit: 04221336bc9eed46c05ed1e828a6811534d4b4ab
ms.translationtype: MT
ms.contentlocale: sv-SE
ms.lasthandoff: 12/08/2020
ms.locfileid: "98414568"
---
# <span data-ttu-id="f575c-101">New-AzStorageSyncService</span><span class="sxs-lookup"><span data-stu-id="f575c-101">New-AzStorageSyncService</span></span>

## <span data-ttu-id="f575c-102">Sammanfattning</span><span class="sxs-lookup"><span data-stu-id="f575c-102">SYNOPSIS</span></span>
<span data-ttu-id="f575c-103">Det här kommandot skapar en ny lagrings synkroniseringstjänst i en resurs grupp.</span><span class="sxs-lookup"><span data-stu-id="f575c-103">This command creates a new storage sync service in a resource group.</span></span>

## <span data-ttu-id="f575c-104">FRÅGESYNTAXEN</span><span class="sxs-lookup"><span data-stu-id="f575c-104">SYNTAX</span></span>

```
New-AzStorageSyncService [-ResourceGroupName] <String> [-Name] <String> [-Location] <String> [-IncomingTrafficPolicy] <String> [-Tag <Hashtable>]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="f575c-105">PROBLEMBESKRIVNING</span><span class="sxs-lookup"><span data-stu-id="f575c-105">DESCRIPTION</span></span>
<span data-ttu-id="f575c-106">En synkroniseringstjänst för lagring är den högsta nivå resursen för Azure-filsynkronisering. Det här kommandot skapar en ny lagrings synkroniseringstjänst i en resurs grupp.</span><span class="sxs-lookup"><span data-stu-id="f575c-106">A storage sync service is the top level resource for Azure File Sync. This command creates a new storage sync service in a resource group.</span></span> <span data-ttu-id="f575c-107">Vi rekommenderar att du skapar så lite lagrings synctjänster som behövs för att skilja olika grupper av servrar i organisationen.</span><span class="sxs-lookup"><span data-stu-id="f575c-107">We recommend to create as few storage sync services as absolutely necessary to differentiate distinct groups of servers in your organization.</span></span> <span data-ttu-id="f575c-108">En synkroniseringstjänst för lagring innehåller Sync-grupper och fungerar också som ett mål för registrering av dina servrar.</span><span class="sxs-lookup"><span data-stu-id="f575c-108">A storage sync service contains sync groups and also works as a target to register your servers to.</span></span> <span data-ttu-id="f575c-109">En server kan bara vara registrerad på en enda lagrings synkroniseringstjänst.</span><span class="sxs-lookup"><span data-stu-id="f575c-109">A server can only be registered to a single storage sync service.</span></span> <span data-ttu-id="f575c-110">Om servrar någonsin behöver delta i synkroniseringen av samma uppsättning filer registrerar du dem på samma synkroniseringstjänst för lagring.</span><span class="sxs-lookup"><span data-stu-id="f575c-110">If servers ever need to participate in syncing the same set of files, register them to the same storage sync service.</span></span>

## <span data-ttu-id="f575c-111">BESKRIVS</span><span class="sxs-lookup"><span data-stu-id="f575c-111">EXAMPLES</span></span>

### <span data-ttu-id="f575c-112">Exempel 1</span><span class="sxs-lookup"><span data-stu-id="f575c-112">Example 1</span></span>
```powershell
PS C:\> New-AzStorageSyncService -ResourceGroupName "myResourceGroup" -Location "myLocation" -StorageSyncServiceName "myStorageSyncServiceName" -IncomingTrafficPolicy "AllowAllTraffic"
```

<span data-ttu-id="f575c-113">Det här kommandot skapar en synkroniseringstjänst för lagring.</span><span class="sxs-lookup"><span data-stu-id="f575c-113">This command will create a storage sync service.</span></span>

## <span data-ttu-id="f575c-114">MALLPARAMETRAR</span><span class="sxs-lookup"><span data-stu-id="f575c-114">PARAMETERS</span></span>

### <span data-ttu-id="f575c-115">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="f575c-115">-DefaultProfile</span></span>
<span data-ttu-id="f575c-116">Autentiseringsuppgifter, konto, klient organisation och abonnemang som används för kommunikation med Azure.</span><span class="sxs-lookup"><span data-stu-id="f575c-116">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="f575c-117">-Plats</span><span class="sxs-lookup"><span data-stu-id="f575c-117">-Location</span></span>
<span data-ttu-id="f575c-118">Plats för lagrings platsen.</span><span class="sxs-lookup"><span data-stu-id="f575c-118">Storage Sync Service location.</span></span>

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

### <span data-ttu-id="f575c-119">-IncomingTrafficPolicy</span><span class="sxs-lookup"><span data-stu-id="f575c-119">-IncomingTrafficPolicy</span></span>
<span data-ttu-id="f575c-120">IncomingTrafficPolicy för Storage Sync-tjänsten</span><span class="sxs-lookup"><span data-stu-id="f575c-120">Storage Sync Service IncomingTrafficPolicy</span></span>

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

### <span data-ttu-id="f575c-121">-Namn</span><span class="sxs-lookup"><span data-stu-id="f575c-121">-Name</span></span>
<span data-ttu-id="f575c-122">Namn på Storage Sync-tjänsten.</span><span class="sxs-lookup"><span data-stu-id="f575c-122">Name of the storage sync service.</span></span>

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

### <span data-ttu-id="f575c-123">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="f575c-123">-ResourceGroupName</span></span>
<span data-ttu-id="f575c-124">Resurs grupps namn.</span><span class="sxs-lookup"><span data-stu-id="f575c-124">Resource Group Name.</span></span>

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

### <span data-ttu-id="f575c-125">-Tagg</span><span class="sxs-lookup"><span data-stu-id="f575c-125">-Tag</span></span>
<span data-ttu-id="f575c-126">Tjänst märkning för Storage Sync.</span><span class="sxs-lookup"><span data-stu-id="f575c-126">Storage Sync Service Tags.</span></span>

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

### <span data-ttu-id="f575c-127">-Bekräfta</span><span class="sxs-lookup"><span data-stu-id="f575c-127">-Confirm</span></span>
<span data-ttu-id="f575c-128">Du uppmanas att bekräfta innan du kör cmdleten.</span><span class="sxs-lookup"><span data-stu-id="f575c-128">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="f575c-129">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="f575c-129">-WhatIf</span></span>
<span data-ttu-id="f575c-130">Visar vad som händer om cmdleten körs.</span><span class="sxs-lookup"><span data-stu-id="f575c-130">Shows what would happen if the cmdlet runs.</span></span> <span data-ttu-id="f575c-131">Cmdleten körs inte.</span><span class="sxs-lookup"><span data-stu-id="f575c-131">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="f575c-132">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="f575c-132">CommonParameters</span></span>
<span data-ttu-id="f575c-133">Den här cmdleten har stöd för de gemensamma parametrarna:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-disvariable,-utbuffer,-PipelineVariable,-verbose,-WarningAction och-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="f575c-133">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="f575c-134">Mer information finns i about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="f575c-134">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="f575c-135">KOSTNADS</span><span class="sxs-lookup"><span data-stu-id="f575c-135">INPUTS</span></span>

### <span data-ttu-id="f575c-136">System. String</span><span class="sxs-lookup"><span data-stu-id="f575c-136">System.String</span></span>

## <span data-ttu-id="f575c-137">VÄRDEN</span><span class="sxs-lookup"><span data-stu-id="f575c-137">OUTPUTS</span></span>

### <span data-ttu-id="f575c-138">Microsoft. Azure. commands. StorageSync. Models. PSStorageSyncService</span><span class="sxs-lookup"><span data-stu-id="f575c-138">Microsoft.Azure.Commands.StorageSync.Models.PSStorageSyncService</span></span>

## <span data-ttu-id="f575c-139">ANMÄRKNINGAR</span><span class="sxs-lookup"><span data-stu-id="f575c-139">NOTES</span></span>

## <span data-ttu-id="f575c-140">RELATERADE LÄNKAR</span><span class="sxs-lookup"><span data-stu-id="f575c-140">RELATED LINKS</span></span>
