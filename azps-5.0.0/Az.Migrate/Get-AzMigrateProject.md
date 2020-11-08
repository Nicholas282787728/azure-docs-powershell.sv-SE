---
external help file: ''
Module Name: Az.Migrate
online version: https://docs.microsoft.com/en-us/powershell/module/az.migrate/get-azmigrateproject
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Migrate/help/Get-AzMigrateProject.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Migrate/help/Get-AzMigrateProject.md
ms.openlocfilehash: 1e3fdb2eabd986907a4b702a62caa3a0d9c34e85
ms.sourcegitcommit: b4a38bcb0501a9016a4998efd377aa75d3ef9ce8
ms.translationtype: MT
ms.contentlocale: sv-SE
ms.lasthandoff: 10/27/2020
ms.locfileid: "94273300"
---
# <span data-ttu-id="57028-101">Get-AzMigrateProject</span><span class="sxs-lookup"><span data-stu-id="57028-101">Get-AzMigrateProject</span></span>

## <span data-ttu-id="57028-102">Sammanfattning</span><span class="sxs-lookup"><span data-stu-id="57028-102">SYNOPSIS</span></span>
<span data-ttu-id="57028-103">Metod för att få ett migrera projekt.</span><span class="sxs-lookup"><span data-stu-id="57028-103">Method to get a migrate project.</span></span>

## <span data-ttu-id="57028-104">FRÅGESYNTAXEN</span><span class="sxs-lookup"><span data-stu-id="57028-104">SYNTAX</span></span>

```
Get-AzMigrateProject -Name <String> -ResourceGroupName <String> [-SubscriptionId <String[]>]
 [-DefaultProfile <PSObject>] [<CommonParameters>]
```

## <span data-ttu-id="57028-105">PROBLEMBESKRIVNING</span><span class="sxs-lookup"><span data-stu-id="57028-105">DESCRIPTION</span></span>
<span data-ttu-id="57028-106">Metod för att få ett migrera projekt.</span><span class="sxs-lookup"><span data-stu-id="57028-106">Method to get a migrate project.</span></span>

## <span data-ttu-id="57028-107">BESKRIVS</span><span class="sxs-lookup"><span data-stu-id="57028-107">EXAMPLES</span></span>

### <span data-ttu-id="57028-108">Exempel 1: skaffa</span><span class="sxs-lookup"><span data-stu-id="57028-108">Example 1: Get</span></span>
```powershell
PS C:\> Get-AzMigrateProject -SubscriptionId xxx-xxx-xxx -ResourceGroupName BugBashAVSVMware -Name BugBashAVSVMware

ETag Location      Name             Type
---- --------      ----             ----
     southeastasia BugBashAVSVMware Microsoft.Migrate/MigrateProjects
```

<span data-ttu-id="57028-109">Metod för att få ett migrera projekt.</span><span class="sxs-lookup"><span data-stu-id="57028-109">Method to get a migrate project.</span></span>

## <span data-ttu-id="57028-110">MALLPARAMETRAR</span><span class="sxs-lookup"><span data-stu-id="57028-110">PARAMETERS</span></span>

### <span data-ttu-id="57028-111">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="57028-111">-DefaultProfile</span></span>
<span data-ttu-id="57028-112">Autentiseringsuppgifter, konto, klient organisation och abonnemang som används för kommunikation med Azure.</span><span class="sxs-lookup"><span data-stu-id="57028-112">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="57028-113">-Namn</span><span class="sxs-lookup"><span data-stu-id="57028-113">-Name</span></span>
<span data-ttu-id="57028-114">Namn på Azure Migrate Project.</span><span class="sxs-lookup"><span data-stu-id="57028-114">Name of the Azure Migrate project.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases: MigrateProjectName

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="57028-115">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="57028-115">-ResourceGroupName</span></span>
<span data-ttu-id="57028-116">Namnet på den Azure Resource-grupp som migrerar Project.</span><span class="sxs-lookup"><span data-stu-id="57028-116">Name of the Azure Resource Group that migrate project is part of.</span></span>

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

### <span data-ttu-id="57028-117">-SubscriptionId</span><span class="sxs-lookup"><span data-stu-id="57028-117">-SubscriptionId</span></span>
<span data-ttu-id="57028-118">ID för Azure-prenumeration som migrerar projektet skapades med.</span><span class="sxs-lookup"><span data-stu-id="57028-118">Azure Subscription Id in which migrate project was created.</span></span>

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

### <span data-ttu-id="57028-119">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="57028-119">CommonParameters</span></span>
<span data-ttu-id="57028-120">Den här cmdleten har stöd för de gemensamma parametrarna:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-disvariable,-utbuffer,-PipelineVariable,-verbose,-WarningAction och-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="57028-120">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="57028-121">Mer information finns i [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="57028-121">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="57028-122">KOSTNADS</span><span class="sxs-lookup"><span data-stu-id="57028-122">INPUTS</span></span>

## <span data-ttu-id="57028-123">VÄRDEN</span><span class="sxs-lookup"><span data-stu-id="57028-123">OUTPUTS</span></span>

### <span data-ttu-id="57028-124">Microsoft. Azure. PowerShell. cmdletar. Migrate. Models. Api20180901Preview. IMigrateProject</span><span class="sxs-lookup"><span data-stu-id="57028-124">Microsoft.Azure.PowerShell.Cmdlets.Migrate.Models.Api20180901Preview.IMigrateProject</span></span>

## <span data-ttu-id="57028-125">ANMÄRKNINGAR</span><span class="sxs-lookup"><span data-stu-id="57028-125">NOTES</span></span>

<span data-ttu-id="57028-126">ALIAS</span><span class="sxs-lookup"><span data-stu-id="57028-126">ALIASES</span></span>

## <span data-ttu-id="57028-127">RELATERADE LÄNKAR</span><span class="sxs-lookup"><span data-stu-id="57028-127">RELATED LINKS</span></span>

