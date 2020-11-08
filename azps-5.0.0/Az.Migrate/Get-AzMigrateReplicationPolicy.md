---
external help file: ''
Module Name: Az.Migrate
online version: https://docs.microsoft.com/en-us/powershell/module/az.migrate/get-azmigratereplicationpolicy
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Migrate/help/Get-AzMigrateReplicationPolicy.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Migrate/help/Get-AzMigrateReplicationPolicy.md
ms.openlocfilehash: a5e35096966355a69ad5b363b61ab3cd5d2f0d0b
ms.sourcegitcommit: b4a38bcb0501a9016a4998efd377aa75d3ef9ce8
ms.translationtype: MT
ms.contentlocale: sv-SE
ms.lasthandoff: 10/27/2020
ms.locfileid: "94273298"
---
# <span data-ttu-id="37d66-101">Get-AzMigrateReplicationPolicy</span><span class="sxs-lookup"><span data-stu-id="37d66-101">Get-AzMigrateReplicationPolicy</span></span>

## <span data-ttu-id="37d66-102">Sammanfattning</span><span class="sxs-lookup"><span data-stu-id="37d66-102">SYNOPSIS</span></span>
<span data-ttu-id="37d66-103">Hämtar information om en replikeringsprincip.</span><span class="sxs-lookup"><span data-stu-id="37d66-103">Gets the details of a replication policy.</span></span>

## <span data-ttu-id="37d66-104">FRÅGESYNTAXEN</span><span class="sxs-lookup"><span data-stu-id="37d66-104">SYNTAX</span></span>

### <span data-ttu-id="37d66-105">Lista (standard)</span><span class="sxs-lookup"><span data-stu-id="37d66-105">List (Default)</span></span>
```
Get-AzMigrateReplicationPolicy -ResourceGroupName <String> -ResourceName <String> [-SubscriptionId <String[]>]
 [-DefaultProfile <PSObject>] [<CommonParameters>]
```

### <span data-ttu-id="37d66-106">Lära</span><span class="sxs-lookup"><span data-stu-id="37d66-106">Get</span></span>
```
Get-AzMigrateReplicationPolicy -PolicyName <String> -ResourceGroupName <String> -ResourceName <String>
 [-SubscriptionId <String[]>] [-DefaultProfile <PSObject>] [<CommonParameters>]
```

## <span data-ttu-id="37d66-107">PROBLEMBESKRIVNING</span><span class="sxs-lookup"><span data-stu-id="37d66-107">DESCRIPTION</span></span>
<span data-ttu-id="37d66-108">Hämtar information om en replikeringsprincip.</span><span class="sxs-lookup"><span data-stu-id="37d66-108">Gets the details of a replication policy.</span></span>

## <span data-ttu-id="37d66-109">BESKRIVS</span><span class="sxs-lookup"><span data-stu-id="37d66-109">EXAMPLES</span></span>

### <span data-ttu-id="37d66-110">Exempel 1: Hämta alla principer i ett valv</span><span class="sxs-lookup"><span data-stu-id="37d66-110">Example 1: Get all policies in a vault</span></span>
```powershell
PS C:\> Get-AzMigrateReplicationPolicy -ResourceGroupName azmigratepwshtestasr13072020 -ResourceName AzMigrateTestProjectPWSH02aarsvault

Location Name                                Type
-------- ----                                ----
         samplepolicy2                       Microsoft.RecoveryServices/vaults/replicationPolicies
         samplepolicy1                       Microsoft.RecoveryServices/vaults/replicationPolicies
         samplePolicy3                       Microsoft.RecoveryServices/vaults/replicationPolicies
         migrateAzMigratePWSHTc8d1sitepolicy Microsoft.RecoveryServices/vaults/replicationPolicies
```

<span data-ttu-id="37d66-111">Skaffa alla principer.</span><span class="sxs-lookup"><span data-stu-id="37d66-111">Get all policies.</span></span>

### <span data-ttu-id="37d66-112">Exempel 2: skaffa en specifik policy</span><span class="sxs-lookup"><span data-stu-id="37d66-112">Example 2: Get a specific policy</span></span>
```powershell
PS C:\> Get-AzMigrateReplicationPolicy -ResourceGroupName azmigratepwshtestasr13072020 -ResourceName AzMigrateTestProjectPWSH02aarsvault -PolicyName  migrateAzMigratePWSHTc8d1sitepolicy

Location Name                                Type
-------- ----                                ----
         migrateAzMigratePWSHTc8d1sitepolicy Microsoft.RecoveryServices/vaults/replicationPolicies
```

<span data-ttu-id="37d66-113">Skaffa ett specifikt namn.</span><span class="sxs-lookup"><span data-stu-id="37d66-113">Get a specific one.</span></span>

## <span data-ttu-id="37d66-114">MALLPARAMETRAR</span><span class="sxs-lookup"><span data-stu-id="37d66-114">PARAMETERS</span></span>

### <span data-ttu-id="37d66-115">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="37d66-115">-DefaultProfile</span></span>
<span data-ttu-id="37d66-116">Autentiseringsuppgifter, konto, klient organisation och abonnemang som används för kommunikation med Azure.</span><span class="sxs-lookup"><span data-stu-id="37d66-116">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="37d66-117">-PolicyName</span><span class="sxs-lookup"><span data-stu-id="37d66-117">-PolicyName</span></span>
<span data-ttu-id="37d66-118">Namn på replikeringsprincip.</span><span class="sxs-lookup"><span data-stu-id="37d66-118">Replication policy name.</span></span>

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

### <span data-ttu-id="37d66-119">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="37d66-119">-ResourceGroupName</span></span>
<span data-ttu-id="37d66-120">Namnet på resurs gruppen där Recovery Services-valvet finns.</span><span class="sxs-lookup"><span data-stu-id="37d66-120">The name of the resource group where the recovery services vault is present.</span></span>

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

### <span data-ttu-id="37d66-121">-ResourceName</span><span class="sxs-lookup"><span data-stu-id="37d66-121">-ResourceName</span></span>
<span data-ttu-id="37d66-122">Namnet på Recovery Services-valvet.</span><span class="sxs-lookup"><span data-stu-id="37d66-122">The name of the recovery services vault.</span></span>

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

### <span data-ttu-id="37d66-123">-SubscriptionId</span><span class="sxs-lookup"><span data-stu-id="37d66-123">-SubscriptionId</span></span>
<span data-ttu-id="37d66-124">Abonnemangs-ID.</span><span class="sxs-lookup"><span data-stu-id="37d66-124">The subscription Id.</span></span>

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

### <span data-ttu-id="37d66-125">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="37d66-125">CommonParameters</span></span>
<span data-ttu-id="37d66-126">Den här cmdleten har stöd för de gemensamma parametrarna:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-disvariable,-utbuffer,-PipelineVariable,-verbose,-WarningAction och-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="37d66-126">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="37d66-127">Mer information finns i [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="37d66-127">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="37d66-128">KOSTNADS</span><span class="sxs-lookup"><span data-stu-id="37d66-128">INPUTS</span></span>

## <span data-ttu-id="37d66-129">VÄRDEN</span><span class="sxs-lookup"><span data-stu-id="37d66-129">OUTPUTS</span></span>

### <span data-ttu-id="37d66-130">Microsoft. Azure. PowerShell. cmdletar. Migrate. Models. Api20180110. IPolicy</span><span class="sxs-lookup"><span data-stu-id="37d66-130">Microsoft.Azure.PowerShell.Cmdlets.Migrate.Models.Api20180110.IPolicy</span></span>

## <span data-ttu-id="37d66-131">ANMÄRKNINGAR</span><span class="sxs-lookup"><span data-stu-id="37d66-131">NOTES</span></span>

<span data-ttu-id="37d66-132">ALIAS</span><span class="sxs-lookup"><span data-stu-id="37d66-132">ALIASES</span></span>

## <span data-ttu-id="37d66-133">RELATERADE LÄNKAR</span><span class="sxs-lookup"><span data-stu-id="37d66-133">RELATED LINKS</span></span>

