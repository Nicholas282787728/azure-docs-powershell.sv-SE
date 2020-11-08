---
external help file: ''
Module Name: Az.Migrate
online version: https://docs.microsoft.com/en-us/powershell/module/az.migrate/get-azmigratesite
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Migrate/help/Get-AzMigrateSite.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Migrate/help/Get-AzMigrateSite.md
ms.openlocfilehash: ebea7936483a34d2515c69c416146d07651b396b
ms.sourcegitcommit: b4a38bcb0501a9016a4998efd377aa75d3ef9ce8
ms.translationtype: MT
ms.contentlocale: sv-SE
ms.lasthandoff: 10/27/2020
ms.locfileid: "94272104"
---
# <span data-ttu-id="ff9a2-101">Get-AzMigrateSite</span><span class="sxs-lookup"><span data-stu-id="ff9a2-101">Get-AzMigrateSite</span></span>

## <span data-ttu-id="ff9a2-102">Sammanfattning</span><span class="sxs-lookup"><span data-stu-id="ff9a2-102">SYNOPSIS</span></span>
<span data-ttu-id="ff9a2-103">Metod för att hämta en webbplats.</span><span class="sxs-lookup"><span data-stu-id="ff9a2-103">Method to get a site.</span></span>

## <span data-ttu-id="ff9a2-104">FRÅGESYNTAXEN</span><span class="sxs-lookup"><span data-stu-id="ff9a2-104">SYNTAX</span></span>

```
Get-AzMigrateSite -Name <String> -ResourceGroupName <String> [-SubscriptionId <String[]>]
 [-DefaultProfile <PSObject>] [<CommonParameters>]
```

## <span data-ttu-id="ff9a2-105">PROBLEMBESKRIVNING</span><span class="sxs-lookup"><span data-stu-id="ff9a2-105">DESCRIPTION</span></span>
<span data-ttu-id="ff9a2-106">Metod för att hämta en webbplats.</span><span class="sxs-lookup"><span data-stu-id="ff9a2-106">Method to get a site.</span></span>

## <span data-ttu-id="ff9a2-107">BESKRIVS</span><span class="sxs-lookup"><span data-stu-id="ff9a2-107">EXAMPLES</span></span>

### <span data-ttu-id="ff9a2-108">Exempel 1: Get (standard)</span><span class="sxs-lookup"><span data-stu-id="ff9a2-108">Example 1: Get (Default)</span></span>
```powershell
PS C:\> Get-AzMigrateSite -SubscriptionId xxx-xxx-xxx -ResourceGroupName BugBashAVSVMware -SiteName BBVMwareAVScbbcsite

ETag Location      Name                Type
---- --------      ----                ----
     southeastasia BBVMwareAVScbbcsite Microsoft.OffAzure/VMwareSites

```

<span data-ttu-id="ff9a2-109">Hämta webbplats med namn</span><span class="sxs-lookup"><span data-stu-id="ff9a2-109">Get site by name</span></span>

## <span data-ttu-id="ff9a2-110">MALLPARAMETRAR</span><span class="sxs-lookup"><span data-stu-id="ff9a2-110">PARAMETERS</span></span>

### <span data-ttu-id="ff9a2-111">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="ff9a2-111">-DefaultProfile</span></span>
<span data-ttu-id="ff9a2-112">Autentiseringsuppgifter, konto, klient organisation och abonnemang som används för kommunikation med Azure.</span><span class="sxs-lookup"><span data-stu-id="ff9a2-112">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="ff9a2-113">-Namn</span><span class="sxs-lookup"><span data-stu-id="ff9a2-113">-Name</span></span>
<span data-ttu-id="ff9a2-114">Webbplats namn.</span><span class="sxs-lookup"><span data-stu-id="ff9a2-114">Site name.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases: SiteName

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="ff9a2-115">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="ff9a2-115">-ResourceGroupName</span></span>
<span data-ttu-id="ff9a2-116">Namnet på resurs gruppen.</span><span class="sxs-lookup"><span data-stu-id="ff9a2-116">The name of the resource group.</span></span>
<span data-ttu-id="ff9a2-117">Namnet är Skift läges okänsligt.</span><span class="sxs-lookup"><span data-stu-id="ff9a2-117">The name is case insensitive.</span></span>

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

### <span data-ttu-id="ff9a2-118">-SubscriptionId</span><span class="sxs-lookup"><span data-stu-id="ff9a2-118">-SubscriptionId</span></span>
<span data-ttu-id="ff9a2-119">ID för mål prenumerationen.</span><span class="sxs-lookup"><span data-stu-id="ff9a2-119">The ID of the target subscription.</span></span>

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

### <span data-ttu-id="ff9a2-120">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="ff9a2-120">CommonParameters</span></span>
<span data-ttu-id="ff9a2-121">Den här cmdleten har stöd för de gemensamma parametrarna:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-disvariable,-utbuffer,-PipelineVariable,-verbose,-WarningAction och-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="ff9a2-121">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="ff9a2-122">Mer information finns i [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="ff9a2-122">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="ff9a2-123">KOSTNADS</span><span class="sxs-lookup"><span data-stu-id="ff9a2-123">INPUTS</span></span>

## <span data-ttu-id="ff9a2-124">VÄRDEN</span><span class="sxs-lookup"><span data-stu-id="ff9a2-124">OUTPUTS</span></span>

### <span data-ttu-id="ff9a2-125">Microsoft. Azure. PowerShell. cmdletar. Migrate. Models. Api202001. IVMwareSite</span><span class="sxs-lookup"><span data-stu-id="ff9a2-125">Microsoft.Azure.PowerShell.Cmdlets.Migrate.Models.Api202001.IVMwareSite</span></span>

## <span data-ttu-id="ff9a2-126">ANMÄRKNINGAR</span><span class="sxs-lookup"><span data-stu-id="ff9a2-126">NOTES</span></span>

<span data-ttu-id="ff9a2-127">ALIAS</span><span class="sxs-lookup"><span data-stu-id="ff9a2-127">ALIASES</span></span>

## <span data-ttu-id="ff9a2-128">RELATERADE LÄNKAR</span><span class="sxs-lookup"><span data-stu-id="ff9a2-128">RELATED LINKS</span></span>

