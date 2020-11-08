---
external help file: ''
Module Name: Az.Migrate
online version: https://docs.microsoft.com/en-us/powershell/module/az.migrate/get-azmigratesolution
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Migrate/help/Get-AzMigrateSolution.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Migrate/help/Get-AzMigrateSolution.md
ms.openlocfilehash: 62b43668e8d886a11a26204edcd3c8b13635eff4
ms.sourcegitcommit: b4a38bcb0501a9016a4998efd377aa75d3ef9ce8
ms.translationtype: MT
ms.contentlocale: sv-SE
ms.lasthandoff: 10/27/2020
ms.locfileid: "94272101"
---
# <span data-ttu-id="712dd-101">Get-AzMigrateSolution</span><span class="sxs-lookup"><span data-stu-id="712dd-101">Get-AzMigrateSolution</span></span>

## <span data-ttu-id="712dd-102">Sammanfattning</span><span class="sxs-lookup"><span data-stu-id="712dd-102">SYNOPSIS</span></span>
<span data-ttu-id="712dd-103">Hämtar en lösning i det migrerande projektet.</span><span class="sxs-lookup"><span data-stu-id="712dd-103">Gets a solution in the migrate project.</span></span>

## <span data-ttu-id="712dd-104">FRÅGESYNTAXEN</span><span class="sxs-lookup"><span data-stu-id="712dd-104">SYNTAX</span></span>

```
Get-AzMigrateSolution -MigrateProjectName <String> -Name <String> -ResourceGroupName <String>
 [-SubscriptionId <String[]>] [-DefaultProfile <PSObject>] [<CommonParameters>]
```

## <span data-ttu-id="712dd-105">PROBLEMBESKRIVNING</span><span class="sxs-lookup"><span data-stu-id="712dd-105">DESCRIPTION</span></span>
<span data-ttu-id="712dd-106">Hämtar en lösning i det migrerande projektet.</span><span class="sxs-lookup"><span data-stu-id="712dd-106">Gets a solution in the migrate project.</span></span>

## <span data-ttu-id="712dd-107">BESKRIVS</span><span class="sxs-lookup"><span data-stu-id="712dd-107">EXAMPLES</span></span>

### <span data-ttu-id="712dd-108">Exempel 1: skaffa</span><span class="sxs-lookup"><span data-stu-id="712dd-108">Example 1: Get</span></span>
```powershell
PS C:\>Get-AzMigrateSolution -SubscriptionId xxx-xxx-xxx -ResourceGroupName BugBashAVSVMware -MigrateProjectName BugBashAVSVMware -Name Servers-Migration-ServerMigration

Etag                                   Name                              Type
----                                   ----                              ----
"010097f1-0000-1800-0000-5ee9ae2b0000" Servers-Migration-ServerMigration Microsoft.Migrate/MigrateProjec…
```

<span data-ttu-id="712dd-109">Migrera Project-lösning efter namn.</span><span class="sxs-lookup"><span data-stu-id="712dd-109">Get Migrate project solution by name.</span></span>

## <span data-ttu-id="712dd-110">MALLPARAMETRAR</span><span class="sxs-lookup"><span data-stu-id="712dd-110">PARAMETERS</span></span>

### <span data-ttu-id="712dd-111">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="712dd-111">-DefaultProfile</span></span>
<span data-ttu-id="712dd-112">Autentiseringsuppgifter, konto, klient organisation och abonnemang som används för kommunikation med Azure.</span><span class="sxs-lookup"><span data-stu-id="712dd-112">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="712dd-113">-MigrateProjectName</span><span class="sxs-lookup"><span data-stu-id="712dd-113">-MigrateProjectName</span></span>
<span data-ttu-id="712dd-114">Namn på Azure Migrate Project.</span><span class="sxs-lookup"><span data-stu-id="712dd-114">Name of the Azure Migrate project.</span></span>

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

### <span data-ttu-id="712dd-115">-Namn</span><span class="sxs-lookup"><span data-stu-id="712dd-115">-Name</span></span>
<span data-ttu-id="712dd-116">Unikt namn på en migrations lösning i ett migrerat projekt.</span><span class="sxs-lookup"><span data-stu-id="712dd-116">Unique name of a migration solution within a migrate project.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases: SolutionName

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="712dd-117">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="712dd-117">-ResourceGroupName</span></span>
<span data-ttu-id="712dd-118">Namnet på den Azure Resource-grupp som migrerar Project.</span><span class="sxs-lookup"><span data-stu-id="712dd-118">Name of the Azure Resource Group that migrate project is part of.</span></span>

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

### <span data-ttu-id="712dd-119">-SubscriptionId</span><span class="sxs-lookup"><span data-stu-id="712dd-119">-SubscriptionId</span></span>
<span data-ttu-id="712dd-120">ID för Azure-prenumeration som migrerar projektet skapades med.</span><span class="sxs-lookup"><span data-stu-id="712dd-120">Azure Subscription Id in which migrate project was created.</span></span>

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

### <span data-ttu-id="712dd-121">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="712dd-121">CommonParameters</span></span>
<span data-ttu-id="712dd-122">Den här cmdleten har stöd för de gemensamma parametrarna:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-disvariable,-utbuffer,-PipelineVariable,-verbose,-WarningAction och-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="712dd-122">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="712dd-123">Mer information finns i [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="712dd-123">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="712dd-124">KOSTNADS</span><span class="sxs-lookup"><span data-stu-id="712dd-124">INPUTS</span></span>

## <span data-ttu-id="712dd-125">VÄRDEN</span><span class="sxs-lookup"><span data-stu-id="712dd-125">OUTPUTS</span></span>

### <span data-ttu-id="712dd-126">Microsoft. Azure. PowerShell. cmdletar. Migrate. Models. Api20180901Preview. ISolution</span><span class="sxs-lookup"><span data-stu-id="712dd-126">Microsoft.Azure.PowerShell.Cmdlets.Migrate.Models.Api20180901Preview.ISolution</span></span>

## <span data-ttu-id="712dd-127">ANMÄRKNINGAR</span><span class="sxs-lookup"><span data-stu-id="712dd-127">NOTES</span></span>

<span data-ttu-id="712dd-128">ALIAS</span><span class="sxs-lookup"><span data-stu-id="712dd-128">ALIASES</span></span>

## <span data-ttu-id="712dd-129">RELATERADE LÄNKAR</span><span class="sxs-lookup"><span data-stu-id="712dd-129">RELATED LINKS</span></span>

