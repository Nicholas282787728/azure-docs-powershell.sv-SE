---
external help file: ''
Module Name: Az.Migrate
online version: https://docs.microsoft.com/en-us/powershell/module/az.migrate/get-azmigratereplicationprotectioncontainer
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Migrate/help/Get-AzMigrateReplicationProtectionContainer.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Migrate/help/Get-AzMigrateReplicationProtectionContainer.md
ms.openlocfilehash: a89d762f0317075a0da94290ad964aeef133fdd5
ms.sourcegitcommit: 04221336bc9eed46c05ed1e828a6811534d4b4ab
ms.translationtype: MT
ms.contentlocale: sv-SE
ms.lasthandoff: 12/08/2020
ms.locfileid: "98390219"
---
# <span data-ttu-id="a5a85-101">Get-AzMigrateReplicationProtectionContainer</span><span class="sxs-lookup"><span data-stu-id="a5a85-101">Get-AzMigrateReplicationProtectionContainer</span></span>

## <span data-ttu-id="a5a85-102">Sammanfattning</span><span class="sxs-lookup"><span data-stu-id="a5a85-102">SYNOPSIS</span></span>
<span data-ttu-id="a5a85-103">Hämtar information om en skydds behållare.</span><span class="sxs-lookup"><span data-stu-id="a5a85-103">Gets the details of a protection container.</span></span>

## <span data-ttu-id="a5a85-104">FRÅGESYNTAXEN</span><span class="sxs-lookup"><span data-stu-id="a5a85-104">SYNTAX</span></span>

### <span data-ttu-id="a5a85-105">Lista (standard)</span><span class="sxs-lookup"><span data-stu-id="a5a85-105">List (Default)</span></span>
```
Get-AzMigrateReplicationProtectionContainer -ResourceGroupName <String> -ResourceName <String>
 [-SubscriptionId <String[]>] [-DefaultProfile <PSObject>] [<CommonParameters>]
```

### <span data-ttu-id="a5a85-106">Lära</span><span class="sxs-lookup"><span data-stu-id="a5a85-106">Get</span></span>
```
Get-AzMigrateReplicationProtectionContainer -FabricName <String> -ProtectionContainerName <String>
 -ResourceGroupName <String> -ResourceName <String> [-SubscriptionId <String[]>] [-DefaultProfile <PSObject>]
 [<CommonParameters>]
```

### <span data-ttu-id="a5a85-107">List1</span><span class="sxs-lookup"><span data-stu-id="a5a85-107">List1</span></span>
```
Get-AzMigrateReplicationProtectionContainer -FabricName <String> -ResourceGroupName <String>
 -ResourceName <String> [-SubscriptionId <String[]>] [-DefaultProfile <PSObject>] [<CommonParameters>]
```

## <span data-ttu-id="a5a85-108">PROBLEMBESKRIVNING</span><span class="sxs-lookup"><span data-stu-id="a5a85-108">DESCRIPTION</span></span>
<span data-ttu-id="a5a85-109">Hämtar information om en skydds behållare.</span><span class="sxs-lookup"><span data-stu-id="a5a85-109">Gets the details of a protection container.</span></span>

## <span data-ttu-id="a5a85-110">BESKRIVS</span><span class="sxs-lookup"><span data-stu-id="a5a85-110">EXAMPLES</span></span>

### <span data-ttu-id="a5a85-111">Exempel 1: lista alla skydds behållare i valvet och Fabric</span><span class="sxs-lookup"><span data-stu-id="a5a85-111">Example 1: List all protection containers in vault and fabric</span></span>
```powershell
PS C:\> PS /src/Migrate [Az.Migrate]> Get-AzMigrateReplicationProtectionContainer -ResourceGroupName azmigratepwshtestasr13072020  -ResourceName AzMigrateTestProjectPWSH02aarsvault -FabricName AzMigratePWSHTc8d1replicationfabric

Location Name                                   Type
-------- ----                                   ----
         AzMigratePWSHTc8d1replicationcontainer Microsoft.RecoveryServices/vaults/replicationFabrics/replicationProtectionContainers
```

<span data-ttu-id="a5a85-112">Visar alla.</span><span class="sxs-lookup"><span data-stu-id="a5a85-112">Lists all.</span></span>

### <span data-ttu-id="a5a85-113">Exempel 2: Hämta en specifik behållare</span><span class="sxs-lookup"><span data-stu-id="a5a85-113">Example 2: Get a specific container</span></span>
```powershell
PS C:\> PS /src/Migrate [Az.Migrate]> Get-AzMigrateReplicationProtectionContainer -ResourceGroupName azmigratepwshtestasr13072020  -ResourceName AzMigrateTestProjectPWSH02aarsvault -FabricName AzMigratePWSHTc8d1replicationfabric -ProtectionContainerName AzMigratePWSHTc8d1replicationcontainer

Location Name                                   Type
-------- ----                                   ----
         AzMigratePWSHTc8d1replicationcontainer Microsoft.RecoveryServices/vaults/replicationFabrics/replicationProtectionContainers
```

<span data-ttu-id="a5a85-114">Får ett specifikt namn.</span><span class="sxs-lookup"><span data-stu-id="a5a85-114">Gets a specific one.</span></span>

## <span data-ttu-id="a5a85-115">MALLPARAMETRAR</span><span class="sxs-lookup"><span data-stu-id="a5a85-115">PARAMETERS</span></span>

### <span data-ttu-id="a5a85-116">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="a5a85-116">-DefaultProfile</span></span>
<span data-ttu-id="a5a85-117">Autentiseringsuppgifter, konto, klient organisation och abonnemang som används för kommunikation med Azure.</span><span class="sxs-lookup"><span data-stu-id="a5a85-117">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="a5a85-118">-FabricName</span><span class="sxs-lookup"><span data-stu-id="a5a85-118">-FabricName</span></span>
<span data-ttu-id="a5a85-119">Fabric-namn.</span><span class="sxs-lookup"><span data-stu-id="a5a85-119">Fabric name.</span></span>

```yaml
Type: System.String
Parameter Sets: Get, List1
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="a5a85-120">-ProtectionContainerName</span><span class="sxs-lookup"><span data-stu-id="a5a85-120">-ProtectionContainerName</span></span>
<span data-ttu-id="a5a85-121">Namn på skydds behållare.</span><span class="sxs-lookup"><span data-stu-id="a5a85-121">Protection container name.</span></span>

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

### <span data-ttu-id="a5a85-122">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="a5a85-122">-ResourceGroupName</span></span>
<span data-ttu-id="a5a85-123">Namnet på resurs gruppen där Recovery Services-valvet finns.</span><span class="sxs-lookup"><span data-stu-id="a5a85-123">The name of the resource group where the recovery services vault is present.</span></span>

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

### <span data-ttu-id="a5a85-124">-ResourceName</span><span class="sxs-lookup"><span data-stu-id="a5a85-124">-ResourceName</span></span>
<span data-ttu-id="a5a85-125">Namnet på Recovery Services-valvet.</span><span class="sxs-lookup"><span data-stu-id="a5a85-125">The name of the recovery services vault.</span></span>

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

### <span data-ttu-id="a5a85-126">-SubscriptionId</span><span class="sxs-lookup"><span data-stu-id="a5a85-126">-SubscriptionId</span></span>
<span data-ttu-id="a5a85-127">Abonnemangs-ID.</span><span class="sxs-lookup"><span data-stu-id="a5a85-127">The subscription Id.</span></span>

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

### <span data-ttu-id="a5a85-128">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="a5a85-128">CommonParameters</span></span>
<span data-ttu-id="a5a85-129">Den här cmdleten har stöd för de gemensamma parametrarna:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-disvariable,-utbuffer,-PipelineVariable,-verbose,-WarningAction och-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="a5a85-129">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="a5a85-130">Mer information finns i [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="a5a85-130">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="a5a85-131">KOSTNADS</span><span class="sxs-lookup"><span data-stu-id="a5a85-131">INPUTS</span></span>

## <span data-ttu-id="a5a85-132">VÄRDEN</span><span class="sxs-lookup"><span data-stu-id="a5a85-132">OUTPUTS</span></span>

### <span data-ttu-id="a5a85-133">Microsoft. Azure. PowerShell. cmdletar. Migrate. Models. Api20180110. IProtectionContainer</span><span class="sxs-lookup"><span data-stu-id="a5a85-133">Microsoft.Azure.PowerShell.Cmdlets.Migrate.Models.Api20180110.IProtectionContainer</span></span>

## <span data-ttu-id="a5a85-134">ANMÄRKNINGAR</span><span class="sxs-lookup"><span data-stu-id="a5a85-134">NOTES</span></span>

<span data-ttu-id="a5a85-135">ALIAS</span><span class="sxs-lookup"><span data-stu-id="a5a85-135">ALIASES</span></span>

## <span data-ttu-id="a5a85-136">RELATERADE LÄNKAR</span><span class="sxs-lookup"><span data-stu-id="a5a85-136">RELATED LINKS</span></span>

