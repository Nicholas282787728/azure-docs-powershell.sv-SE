---
external help file: ''
Module Name: Az.Migrate
online version: https://docs.microsoft.com/en-us/powershell/module/az.migrate/get-azmigratereplicationprotectioncontainermapping
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Migrate/help/Get-AzMigrateReplicationProtectionContainerMapping.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Migrate/help/Get-AzMigrateReplicationProtectionContainerMapping.md
ms.openlocfilehash: e321691106d892c703a56bd94c3fe84ab7d9fe38
ms.sourcegitcommit: b4a38bcb0501a9016a4998efd377aa75d3ef9ce8
ms.translationtype: MT
ms.contentlocale: sv-SE
ms.lasthandoff: 10/27/2020
ms.locfileid: "94273294"
---
# <span data-ttu-id="47d56-101">Get-AzMigrateReplicationProtectionContainerMapping</span><span class="sxs-lookup"><span data-stu-id="47d56-101">Get-AzMigrateReplicationProtectionContainerMapping</span></span>

## <span data-ttu-id="47d56-102">Sammanfattning</span><span class="sxs-lookup"><span data-stu-id="47d56-102">SYNOPSIS</span></span>
<span data-ttu-id="47d56-103">Hämtar information om en mappning för skydds behållare.</span><span class="sxs-lookup"><span data-stu-id="47d56-103">Gets the details of a protection container mapping.</span></span>

## <span data-ttu-id="47d56-104">FRÅGESYNTAXEN</span><span class="sxs-lookup"><span data-stu-id="47d56-104">SYNTAX</span></span>

### <span data-ttu-id="47d56-105">List1 (standard)</span><span class="sxs-lookup"><span data-stu-id="47d56-105">List1 (Default)</span></span>
```
Get-AzMigrateReplicationProtectionContainerMapping -ResourceGroupName <String> -ResourceName <String>
 [-SubscriptionId <String[]>] [-DefaultProfile <PSObject>] [<CommonParameters>]
```

### <span data-ttu-id="47d56-106">Lära</span><span class="sxs-lookup"><span data-stu-id="47d56-106">Get</span></span>
```
Get-AzMigrateReplicationProtectionContainerMapping -FabricName <String> -MappingName <String>
 -ProtectionContainerName <String> -ResourceGroupName <String> -ResourceName <String>
 [-SubscriptionId <String[]>] [-DefaultProfile <PSObject>] [<CommonParameters>]
```

### <span data-ttu-id="47d56-107">Förteckning</span><span class="sxs-lookup"><span data-stu-id="47d56-107">List</span></span>
```
Get-AzMigrateReplicationProtectionContainerMapping -FabricName <String> -ProtectionContainerName <String>
 -ResourceGroupName <String> -ResourceName <String> [-SubscriptionId <String[]>] [-DefaultProfile <PSObject>]
 [<CommonParameters>]
```

## <span data-ttu-id="47d56-108">PROBLEMBESKRIVNING</span><span class="sxs-lookup"><span data-stu-id="47d56-108">DESCRIPTION</span></span>
<span data-ttu-id="47d56-109">Hämtar information om en mappning för skydds behållare.</span><span class="sxs-lookup"><span data-stu-id="47d56-109">Gets the details of a protection container mapping.</span></span>

## <span data-ttu-id="47d56-110">BESKRIVS</span><span class="sxs-lookup"><span data-stu-id="47d56-110">EXAMPLES</span></span>

### <span data-ttu-id="47d56-111">Exempel 1: Hämta en specifik mappning</span><span class="sxs-lookup"><span data-stu-id="47d56-111">Example 1: Get a specific mapping</span></span>
```powershell
PS C:\> Get-AzMigrateReplicationProtectionContainerMapping -ResourceGroupName azmigratepwshtestasr13072020 -ResourceName AzMigrateTestProjectPWSH02aarsvault -FabricName AzMigratePWSHTc8d1replicationfabric -ProtectionContainerName AzMigratePWSHTc8d1replicationcontainer -MappingName "containermapping"

Location Name             Type
-------- ----             ----
         containermapping Microsoft.RecoveryServices/vaults/replicationFabrics/replicationProtectionContainers/replicationProtectionContainerMappings
```

<span data-ttu-id="47d56-112">Få en kart detalj.</span><span class="sxs-lookup"><span data-stu-id="47d56-112">Get a mapping detail.</span></span>

## <span data-ttu-id="47d56-113">MALLPARAMETRAR</span><span class="sxs-lookup"><span data-stu-id="47d56-113">PARAMETERS</span></span>

### <span data-ttu-id="47d56-114">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="47d56-114">-DefaultProfile</span></span>
<span data-ttu-id="47d56-115">Autentiseringsuppgifter, konto, klient organisation och abonnemang som används för kommunikation med Azure.</span><span class="sxs-lookup"><span data-stu-id="47d56-115">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="47d56-116">-FabricName</span><span class="sxs-lookup"><span data-stu-id="47d56-116">-FabricName</span></span>
<span data-ttu-id="47d56-117">Fabric-namn.</span><span class="sxs-lookup"><span data-stu-id="47d56-117">Fabric name.</span></span>

```yaml
Type: System.String
Parameter Sets: Get, List
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="47d56-118">-MappingName</span><span class="sxs-lookup"><span data-stu-id="47d56-118">-MappingName</span></span>
<span data-ttu-id="47d56-119">Mappnings namn för skydds behållare.</span><span class="sxs-lookup"><span data-stu-id="47d56-119">Protection Container mapping name.</span></span>

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

### <span data-ttu-id="47d56-120">-ProtectionContainerName</span><span class="sxs-lookup"><span data-stu-id="47d56-120">-ProtectionContainerName</span></span>
<span data-ttu-id="47d56-121">Namn på skydds behållare.</span><span class="sxs-lookup"><span data-stu-id="47d56-121">Protection container name.</span></span>

```yaml
Type: System.String
Parameter Sets: Get, List
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="47d56-122">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="47d56-122">-ResourceGroupName</span></span>
<span data-ttu-id="47d56-123">Namnet på resurs gruppen där Recovery Services-valvet finns.</span><span class="sxs-lookup"><span data-stu-id="47d56-123">The name of the resource group where the recovery services vault is present.</span></span>

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

### <span data-ttu-id="47d56-124">-ResourceName</span><span class="sxs-lookup"><span data-stu-id="47d56-124">-ResourceName</span></span>
<span data-ttu-id="47d56-125">Namnet på Recovery Services-valvet.</span><span class="sxs-lookup"><span data-stu-id="47d56-125">The name of the recovery services vault.</span></span>

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

### <span data-ttu-id="47d56-126">-SubscriptionId</span><span class="sxs-lookup"><span data-stu-id="47d56-126">-SubscriptionId</span></span>
<span data-ttu-id="47d56-127">Abonnemangs-ID.</span><span class="sxs-lookup"><span data-stu-id="47d56-127">The subscription Id.</span></span>

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

### <span data-ttu-id="47d56-128">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="47d56-128">CommonParameters</span></span>
<span data-ttu-id="47d56-129">Den här cmdleten har stöd för de gemensamma parametrarna:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-disvariable,-utbuffer,-PipelineVariable,-verbose,-WarningAction och-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="47d56-129">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="47d56-130">Mer information finns i [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="47d56-130">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="47d56-131">KOSTNADS</span><span class="sxs-lookup"><span data-stu-id="47d56-131">INPUTS</span></span>

## <span data-ttu-id="47d56-132">VÄRDEN</span><span class="sxs-lookup"><span data-stu-id="47d56-132">OUTPUTS</span></span>

### <span data-ttu-id="47d56-133">Microsoft. Azure. PowerShell. cmdletar. Migrate. Models. Api20180110. IProtectionContainerMapping</span><span class="sxs-lookup"><span data-stu-id="47d56-133">Microsoft.Azure.PowerShell.Cmdlets.Migrate.Models.Api20180110.IProtectionContainerMapping</span></span>

## <span data-ttu-id="47d56-134">ANMÄRKNINGAR</span><span class="sxs-lookup"><span data-stu-id="47d56-134">NOTES</span></span>

<span data-ttu-id="47d56-135">ALIAS</span><span class="sxs-lookup"><span data-stu-id="47d56-135">ALIASES</span></span>

## <span data-ttu-id="47d56-136">RELATERADE LÄNKAR</span><span class="sxs-lookup"><span data-stu-id="47d56-136">RELATED LINKS</span></span>

