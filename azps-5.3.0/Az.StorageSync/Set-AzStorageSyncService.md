---
external help file: Microsoft.Azure.PowerShell.Cmdlets.StorageSync.dll-Help.xml
Module Name: Az.StorageSync
online version: https://docs.microsoft.com/en-us/powershell/module/Az.storagesync/set-Azstoragesyncservice
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/StorageSync/StorageSync/help/Set-AzStorageSyncService.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/StorageSync/StorageSync/help/Set-AzStorageSyncService.md
ms.openlocfilehash: 2e22912df9a567ac836f22c8ac82d0a70610f2f3
ms.sourcegitcommit: 68451baa389791703e666d95469602c5652609ee
ms.translationtype: MT
ms.contentlocale: sv-SE
ms.lasthandoff: 01/05/2021
ms.locfileid: "98521937"
---
# <span data-ttu-id="01c0a-101">Set-AzStorageSyncService</span><span class="sxs-lookup"><span data-stu-id="01c0a-101">Set-AzStorageSyncService</span></span>

## <span data-ttu-id="01c0a-102">Sammanfattning</span><span class="sxs-lookup"><span data-stu-id="01c0a-102">SYNOPSIS</span></span>
<span data-ttu-id="01c0a-103">Det här kommandot anger Storage Sync-tjänsten i en resurs grupp.</span><span class="sxs-lookup"><span data-stu-id="01c0a-103">This command sets storage sync service in a resource group.</span></span>

## <span data-ttu-id="01c0a-104">FRÅGESYNTAXEN</span><span class="sxs-lookup"><span data-stu-id="01c0a-104">SYNTAX</span></span>

```
Set-AzStorageSyncService [-ResourceGroupName] <String> [-Name] <String> [-Location] <String> [-Tag <Hashtable>]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="01c0a-105">PROBLEMBESKRIVNING</span><span class="sxs-lookup"><span data-stu-id="01c0a-105">DESCRIPTION</span></span>
<span data-ttu-id="01c0a-106">En synkroniseringstjänst för lagring är den högsta nivå resursen för Azure-filsynkronisering. Det här kommandot anger Storage Sync-tjänsten i en resurs grupp.</span><span class="sxs-lookup"><span data-stu-id="01c0a-106">A storage sync service is the top level resource for Azure File Sync. This command sets storage sync service in a resource group.</span></span> <span data-ttu-id="01c0a-107">Vi rekommenderar att du skapar så lite lagrings synctjänster som behövs för att skilja olika grupper av servrar i organisationen.</span><span class="sxs-lookup"><span data-stu-id="01c0a-107">We recommend to create as few storage sync services as absolutely necessary to differentiate distinct groups of servers in your organization.</span></span> <span data-ttu-id="01c0a-108">En synkroniseringstjänst för lagring innehåller Sync-grupper och fungerar också som ett mål för registrering av dina servrar.</span><span class="sxs-lookup"><span data-stu-id="01c0a-108">A storage sync service contains sync groups and also works as a target to register your servers to.</span></span> <span data-ttu-id="01c0a-109">En server kan bara vara registrerad på en enda lagrings synkroniseringstjänst.</span><span class="sxs-lookup"><span data-stu-id="01c0a-109">A server can only be registered to a single storage sync service.</span></span> <span data-ttu-id="01c0a-110">Om servrar någonsin behöver delta i synkroniseringen av samma uppsättning filer registrerar du dem på samma synkroniseringstjänst för lagring.</span><span class="sxs-lookup"><span data-stu-id="01c0a-110">If servers ever need to participate in syncing the same set of files, register them to the same storage sync service.</span></span>

## <span data-ttu-id="01c0a-111">BESKRIVS</span><span class="sxs-lookup"><span data-stu-id="01c0a-111">EXAMPLES</span></span>

### <span data-ttu-id="01c0a-112">Exempel 1</span><span class="sxs-lookup"><span data-stu-id="01c0a-112">Example 1</span></span>
```powershell
PS C:\> Set-AzStorageSyncService -ResourceGroupName "myResourceGroup" -StorageSyncServiceName "myStorageSyncServiceName" -IncomingTrafficPolicy "AllowAllTraffic"
```

<span data-ttu-id="01c0a-113">Det här kommandot anger en synkroniseringstjänst för lagring.</span><span class="sxs-lookup"><span data-stu-id="01c0a-113">This command will set a storage sync service.</span></span>

## <span data-ttu-id="01c0a-114">MALLPARAMETRAR</span><span class="sxs-lookup"><span data-stu-id="01c0a-114">PARAMETERS</span></span>

### <span data-ttu-id="01c0a-115">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="01c0a-115">-DefaultProfile</span></span>
<span data-ttu-id="01c0a-116">Autentiseringsuppgifter, konto, klient organisation och abonnemang som används för kommunikation med Azure.</span><span class="sxs-lookup"><span data-stu-id="01c0a-116">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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
### <span data-ttu-id="01c0a-117">-Namn</span><span class="sxs-lookup"><span data-stu-id="01c0a-117">-Name</span></span>
<span data-ttu-id="01c0a-118">Namn på Storage Sync-tjänsten.</span><span class="sxs-lookup"><span data-stu-id="01c0a-118">Name of the storage sync service.</span></span>

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

### <span data-ttu-id="01c0a-119">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="01c0a-119">-ResourceGroupName</span></span>
<span data-ttu-id="01c0a-120">Resurs grupps namn.</span><span class="sxs-lookup"><span data-stu-id="01c0a-120">Resource Group Name.</span></span>

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

### <span data-ttu-id="01c0a-121">-IncomingTrafficPolicy</span><span class="sxs-lookup"><span data-stu-id="01c0a-121">-IncomingTrafficPolicy</span></span>
<span data-ttu-id="01c0a-122">IncomingTrafficPolicy för Storage Sync-tjänsten</span><span class="sxs-lookup"><span data-stu-id="01c0a-122">Storage Sync Service IncomingTrafficPolicy</span></span>

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

### <span data-ttu-id="01c0a-123">-Tagg</span><span class="sxs-lookup"><span data-stu-id="01c0a-123">-Tag</span></span>
<span data-ttu-id="01c0a-124">Tjänst märkning för Storage Sync.</span><span class="sxs-lookup"><span data-stu-id="01c0a-124">Storage Sync Service Tags.</span></span>

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

### <span data-ttu-id="01c0a-125">-Bekräfta</span><span class="sxs-lookup"><span data-stu-id="01c0a-125">-Confirm</span></span>
<span data-ttu-id="01c0a-126">Du uppmanas att bekräfta innan du kör cmdleten.</span><span class="sxs-lookup"><span data-stu-id="01c0a-126">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="01c0a-127">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="01c0a-127">-WhatIf</span></span>
<span data-ttu-id="01c0a-128">Visar vad som händer om cmdleten körs.</span><span class="sxs-lookup"><span data-stu-id="01c0a-128">Shows what would happen if the cmdlet runs.</span></span> <span data-ttu-id="01c0a-129">Cmdleten körs inte.</span><span class="sxs-lookup"><span data-stu-id="01c0a-129">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="01c0a-130">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="01c0a-130">CommonParameters</span></span>
<span data-ttu-id="01c0a-131">Den här cmdleten har stöd för de gemensamma parametrarna:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-disvariable,-utbuffer,-PipelineVariable,-verbose,-WarningAction och-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="01c0a-131">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="01c0a-132">Mer information finns i about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="01c0a-132">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="01c0a-133">KOSTNADS</span><span class="sxs-lookup"><span data-stu-id="01c0a-133">INPUTS</span></span>

### <span data-ttu-id="01c0a-134">System. String</span><span class="sxs-lookup"><span data-stu-id="01c0a-134">System.String</span></span>

## <span data-ttu-id="01c0a-135">VÄRDEN</span><span class="sxs-lookup"><span data-stu-id="01c0a-135">OUTPUTS</span></span>

### <span data-ttu-id="01c0a-136">Microsoft. Azure. commands. StorageSync. Models. PSStorageSyncService</span><span class="sxs-lookup"><span data-stu-id="01c0a-136">Microsoft.Azure.Commands.StorageSync.Models.PSStorageSyncService</span></span>

## <span data-ttu-id="01c0a-137">ANMÄRKNINGAR</span><span class="sxs-lookup"><span data-stu-id="01c0a-137">NOTES</span></span>

## <span data-ttu-id="01c0a-138">RELATERADE LÄNKAR</span><span class="sxs-lookup"><span data-stu-id="01c0a-138">RELATED LINKS</span></span>
