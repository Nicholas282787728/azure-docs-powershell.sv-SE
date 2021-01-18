---
external help file: ''
Module Name: Az.Migrate
online version: https://docs.microsoft.com/en-us/powershell/module/az.migrate/get-azmigraterunasaccount
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Migrate/help/Get-AzMigrateRunAsAccount.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Migrate/help/Get-AzMigrateRunAsAccount.md
ms.openlocfilehash: 6f78a326efc29e3ba89f774575df1c4b7472e70c
ms.sourcegitcommit: 68451baa389791703e666d95469602c5652609ee
ms.translationtype: MT
ms.contentlocale: sv-SE
ms.lasthandoff: 01/05/2021
ms.locfileid: "98521139"
---
# <span data-ttu-id="1b1e0-101">Get-AzMigrateRunAsAccount</span><span class="sxs-lookup"><span data-stu-id="1b1e0-101">Get-AzMigrateRunAsAccount</span></span>

## <span data-ttu-id="1b1e0-102">Sammanfattning</span><span class="sxs-lookup"><span data-stu-id="1b1e0-102">SYNOPSIS</span></span>
<span data-ttu-id="1b1e0-103">Metod för att få kör som-konto.</span><span class="sxs-lookup"><span data-stu-id="1b1e0-103">Method to get run as account.</span></span>

## <span data-ttu-id="1b1e0-104">FRÅGESYNTAXEN</span><span class="sxs-lookup"><span data-stu-id="1b1e0-104">SYNTAX</span></span>

### <span data-ttu-id="1b1e0-105">Lista (standard)</span><span class="sxs-lookup"><span data-stu-id="1b1e0-105">List (Default)</span></span>
```
Get-AzMigrateRunAsAccount -ResourceGroupName <String> -SiteName <String> [-SubscriptionId <String[]>]
 [-DefaultProfile <PSObject>] [<CommonParameters>]
```

### <span data-ttu-id="1b1e0-106">Lära</span><span class="sxs-lookup"><span data-stu-id="1b1e0-106">Get</span></span>
```
Get-AzMigrateRunAsAccount -AccountName <String> -ResourceGroupName <String> -SiteName <String>
 [-SubscriptionId <String[]>] [-DefaultProfile <PSObject>] [<CommonParameters>]
```

## <span data-ttu-id="1b1e0-107">PROBLEMBESKRIVNING</span><span class="sxs-lookup"><span data-stu-id="1b1e0-107">DESCRIPTION</span></span>
<span data-ttu-id="1b1e0-108">Metod för att få kör som-konto.</span><span class="sxs-lookup"><span data-stu-id="1b1e0-108">Method to get run as account.</span></span>

## <span data-ttu-id="1b1e0-109">BESKRIVS</span><span class="sxs-lookup"><span data-stu-id="1b1e0-109">EXAMPLES</span></span>

### <span data-ttu-id="1b1e0-110">Exempel 1: lista (standard)</span><span class="sxs-lookup"><span data-stu-id="1b1e0-110">Example 1: List (Default)</span></span>
```powershell
PS C:\> Get-AzMigrateRunAsAccount  -SubscriptionId xxx-xxx-xxx -ResourceGroupName BugBashAVSVMware -SiteName BBVMwareAVScbbcsite

Name                                 Type
----                                 ----
b090bef3-b733-5e34-bc8f-eb6f2701432a Microsoft.OffAzure/VMwareSites/runasaccounts
```

<span data-ttu-id="1b1e0-111">Visa alla kör som-konton på en webbplats.</span><span class="sxs-lookup"><span data-stu-id="1b1e0-111">List all run as accounts in a site.</span></span>

### <span data-ttu-id="1b1e0-112">Exempel 2: get</span><span class="sxs-lookup"><span data-stu-id="1b1e0-112">Example 2: Get</span></span>
```powershell
PS C:\> Get-AzMigrateRunAsAccount  -SubscriptionId xxx-xxx-xxx -ResourceGroupName BugBashAVSVMware -SiteName BBVMwareAVScbbcsite -AccountName b090bef3-b733-5e34-bc8f-eb6f2701432a

Name                                 Type
----                                 ----
b090bef3-b733-5e34-bc8f-eb6f2701432a Microsoft.OffAzure/VMwareSites/runasaccounts
```

<span data-ttu-id="1b1e0-113">Kör som-konto efter namn.</span><span class="sxs-lookup"><span data-stu-id="1b1e0-113">Get Run as account by name.</span></span>

## <span data-ttu-id="1b1e0-114">MALLPARAMETRAR</span><span class="sxs-lookup"><span data-stu-id="1b1e0-114">PARAMETERS</span></span>

### <span data-ttu-id="1b1e0-115">-AccountName</span><span class="sxs-lookup"><span data-stu-id="1b1e0-115">-AccountName</span></span>
<span data-ttu-id="1b1e0-116">Namn på Kör som-konto.</span><span class="sxs-lookup"><span data-stu-id="1b1e0-116">Run as account ARM name.</span></span>

```yaml
Type: System.String
Parameter Sets: Get
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="1b1e0-117">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="1b1e0-117">-DefaultProfile</span></span>
<span data-ttu-id="1b1e0-118">Autentiseringsuppgifter, konto, klient organisation och abonnemang som används för kommunikation med Azure.</span><span class="sxs-lookup"><span data-stu-id="1b1e0-118">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

```yaml
Type: System.Management.Automation.PSObject
Parameter Sets: (All)
Aliases: AzureRMContext, AzureCredential

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="1b1e0-119">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="1b1e0-119">-ResourceGroupName</span></span>
<span data-ttu-id="1b1e0-120">Namnet på resurs gruppen.</span><span class="sxs-lookup"><span data-stu-id="1b1e0-120">The name of the resource group.</span></span>
<span data-ttu-id="1b1e0-121">Namnet är Skift läges okänsligt.</span><span class="sxs-lookup"><span data-stu-id="1b1e0-121">The name is case insensitive.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="1b1e0-122">-Plats namn</span><span class="sxs-lookup"><span data-stu-id="1b1e0-122">-SiteName</span></span>
<span data-ttu-id="1b1e0-123">Webbplats namn.</span><span class="sxs-lookup"><span data-stu-id="1b1e0-123">Site name.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="1b1e0-124">-SubscriptionId</span><span class="sxs-lookup"><span data-stu-id="1b1e0-124">-SubscriptionId</span></span>
<span data-ttu-id="1b1e0-125">ID för mål prenumerationen.</span><span class="sxs-lookup"><span data-stu-id="1b1e0-125">The ID of the target subscription.</span></span>

```yaml
Type: System.String[]
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: (Get-AzContext).Subscription.Id
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="1b1e0-126">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="1b1e0-126">CommonParameters</span></span>
<span data-ttu-id="1b1e0-127">Den här cmdleten har stöd för de gemensamma parametrarna:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-disvariable,-utbuffer,-PipelineVariable,-verbose,-WarningAction och-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="1b1e0-127">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="1b1e0-128">Mer information finns i [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="1b1e0-128">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="1b1e0-129">KOSTNADS</span><span class="sxs-lookup"><span data-stu-id="1b1e0-129">INPUTS</span></span>

## <span data-ttu-id="1b1e0-130">VÄRDEN</span><span class="sxs-lookup"><span data-stu-id="1b1e0-130">OUTPUTS</span></span>

### <span data-ttu-id="1b1e0-131">Microsoft. Azure. PowerShell. cmdletar. Migrate. Models. Api202001. IVMwareRunAsAccount</span><span class="sxs-lookup"><span data-stu-id="1b1e0-131">Microsoft.Azure.PowerShell.Cmdlets.Migrate.Models.Api202001.IVMwareRunAsAccount</span></span>

## <span data-ttu-id="1b1e0-132">ANMÄRKNINGAR</span><span class="sxs-lookup"><span data-stu-id="1b1e0-132">NOTES</span></span>

<span data-ttu-id="1b1e0-133">ALIAS</span><span class="sxs-lookup"><span data-stu-id="1b1e0-133">ALIASES</span></span>

## <span data-ttu-id="1b1e0-134">RELATERADE LÄNKAR</span><span class="sxs-lookup"><span data-stu-id="1b1e0-134">RELATED LINKS</span></span>

