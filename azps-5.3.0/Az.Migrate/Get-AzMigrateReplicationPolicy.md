---
external help file: ''
Module Name: Az.Migrate
online version: https://docs.microsoft.com/en-us/powershell/module/az.migrate/get-azmigratereplicationpolicy
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Migrate/help/Get-AzMigrateReplicationPolicy.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Migrate/help/Get-AzMigrateReplicationPolicy.md
ms.openlocfilehash: a5e35096966355a69ad5b363b61ab3cd5d2f0d0b
ms.sourcegitcommit: 68451baa389791703e666d95469602c5652609ee
ms.translationtype: MT
ms.contentlocale: sv-SE
ms.lasthandoff: 01/05/2021
ms.locfileid: "98525919"
---
# <span data-ttu-id="36f76-101">Get-AzMigrateReplicationPolicy</span><span class="sxs-lookup"><span data-stu-id="36f76-101">Get-AzMigrateReplicationPolicy</span></span>

## <span data-ttu-id="36f76-102">Sammanfattning</span><span class="sxs-lookup"><span data-stu-id="36f76-102">SYNOPSIS</span></span>
<span data-ttu-id="36f76-103">Hämtar information om en replikeringsprincip.</span><span class="sxs-lookup"><span data-stu-id="36f76-103">Gets the details of a replication policy.</span></span>

## <span data-ttu-id="36f76-104">FRÅGESYNTAXEN</span><span class="sxs-lookup"><span data-stu-id="36f76-104">SYNTAX</span></span>

### <span data-ttu-id="36f76-105">Lista (standard)</span><span class="sxs-lookup"><span data-stu-id="36f76-105">List (Default)</span></span>
```
Get-AzMigrateReplicationPolicy -ResourceGroupName <String> -ResourceName <String> [-SubscriptionId <String[]>]
 [-DefaultProfile <PSObject>] [<CommonParameters>]
```

### <span data-ttu-id="36f76-106">Lära</span><span class="sxs-lookup"><span data-stu-id="36f76-106">Get</span></span>
```
Get-AzMigrateReplicationPolicy -PolicyName <String> -ResourceGroupName <String> -ResourceName <String>
 [-SubscriptionId <String[]>] [-DefaultProfile <PSObject>] [<CommonParameters>]
```

## <span data-ttu-id="36f76-107">PROBLEMBESKRIVNING</span><span class="sxs-lookup"><span data-stu-id="36f76-107">DESCRIPTION</span></span>
<span data-ttu-id="36f76-108">Hämtar information om en replikeringsprincip.</span><span class="sxs-lookup"><span data-stu-id="36f76-108">Gets the details of a replication policy.</span></span>

## <span data-ttu-id="36f76-109">BESKRIVS</span><span class="sxs-lookup"><span data-stu-id="36f76-109">EXAMPLES</span></span>

### <span data-ttu-id="36f76-110">Exempel 1: Hämta alla principer i ett valv</span><span class="sxs-lookup"><span data-stu-id="36f76-110">Example 1: Get all policies in a vault</span></span>
```powershell
PS C:\> Get-AzMigrateReplicationPolicy -ResourceGroupName azmigratepwshtestasr13072020 -ResourceName AzMigrateTestProjectPWSH02aarsvault

Location Name                                Type
-------- ----                                ----
         samplepolicy2                       Microsoft.RecoveryServices/vaults/replicationPolicies
         samplepolicy1                       Microsoft.RecoveryServices/vaults/replicationPolicies
         samplePolicy3                       Microsoft.RecoveryServices/vaults/replicationPolicies
         migrateAzMigratePWSHTc8d1sitepolicy Microsoft.RecoveryServices/vaults/replicationPolicies
```

<span data-ttu-id="36f76-111">Skaffa alla principer.</span><span class="sxs-lookup"><span data-stu-id="36f76-111">Get all policies.</span></span>

### <span data-ttu-id="36f76-112">Exempel 2: skaffa en specifik policy</span><span class="sxs-lookup"><span data-stu-id="36f76-112">Example 2: Get a specific policy</span></span>
```powershell
PS C:\> Get-AzMigrateReplicationPolicy -ResourceGroupName azmigratepwshtestasr13072020 -ResourceName AzMigrateTestProjectPWSH02aarsvault -PolicyName  migrateAzMigratePWSHTc8d1sitepolicy

Location Name                                Type
-------- ----                                ----
         migrateAzMigratePWSHTc8d1sitepolicy Microsoft.RecoveryServices/vaults/replicationPolicies
```

<span data-ttu-id="36f76-113">Skaffa ett specifikt namn.</span><span class="sxs-lookup"><span data-stu-id="36f76-113">Get a specific one.</span></span>

## <span data-ttu-id="36f76-114">MALLPARAMETRAR</span><span class="sxs-lookup"><span data-stu-id="36f76-114">PARAMETERS</span></span>

### <span data-ttu-id="36f76-115">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="36f76-115">-DefaultProfile</span></span>
<span data-ttu-id="36f76-116">Autentiseringsuppgifter, konto, klient organisation och abonnemang som används för kommunikation med Azure.</span><span class="sxs-lookup"><span data-stu-id="36f76-116">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="36f76-117">-PolicyName</span><span class="sxs-lookup"><span data-stu-id="36f76-117">-PolicyName</span></span>
<span data-ttu-id="36f76-118">Namn på replikeringsprincip.</span><span class="sxs-lookup"><span data-stu-id="36f76-118">Replication policy name.</span></span>

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

### <span data-ttu-id="36f76-119">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="36f76-119">-ResourceGroupName</span></span>
<span data-ttu-id="36f76-120">Namnet på resurs gruppen där Recovery Services-valvet finns.</span><span class="sxs-lookup"><span data-stu-id="36f76-120">The name of the resource group where the recovery services vault is present.</span></span>

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

### <span data-ttu-id="36f76-121">-ResourceName</span><span class="sxs-lookup"><span data-stu-id="36f76-121">-ResourceName</span></span>
<span data-ttu-id="36f76-122">Namnet på Recovery Services-valvet.</span><span class="sxs-lookup"><span data-stu-id="36f76-122">The name of the recovery services vault.</span></span>

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

### <span data-ttu-id="36f76-123">-SubscriptionId</span><span class="sxs-lookup"><span data-stu-id="36f76-123">-SubscriptionId</span></span>
<span data-ttu-id="36f76-124">Abonnemangs-ID.</span><span class="sxs-lookup"><span data-stu-id="36f76-124">The subscription Id.</span></span>

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

### <span data-ttu-id="36f76-125">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="36f76-125">CommonParameters</span></span>
<span data-ttu-id="36f76-126">Den här cmdleten har stöd för de gemensamma parametrarna:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-disvariable,-utbuffer,-PipelineVariable,-verbose,-WarningAction och-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="36f76-126">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="36f76-127">Mer information finns i [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="36f76-127">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="36f76-128">KOSTNADS</span><span class="sxs-lookup"><span data-stu-id="36f76-128">INPUTS</span></span>

## <span data-ttu-id="36f76-129">VÄRDEN</span><span class="sxs-lookup"><span data-stu-id="36f76-129">OUTPUTS</span></span>

### <span data-ttu-id="36f76-130">Microsoft. Azure. PowerShell. cmdletar. Migrate. Models. Api20180110. IPolicy</span><span class="sxs-lookup"><span data-stu-id="36f76-130">Microsoft.Azure.PowerShell.Cmdlets.Migrate.Models.Api20180110.IPolicy</span></span>

## <span data-ttu-id="36f76-131">ANMÄRKNINGAR</span><span class="sxs-lookup"><span data-stu-id="36f76-131">NOTES</span></span>

<span data-ttu-id="36f76-132">ALIAS</span><span class="sxs-lookup"><span data-stu-id="36f76-132">ALIASES</span></span>

## <span data-ttu-id="36f76-133">RELATERADE LÄNKAR</span><span class="sxs-lookup"><span data-stu-id="36f76-133">RELATED LINKS</span></span>

