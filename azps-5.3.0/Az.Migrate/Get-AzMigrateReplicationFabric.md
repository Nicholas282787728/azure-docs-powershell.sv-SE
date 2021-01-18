---
external help file: ''
Module Name: Az.Migrate
online version: https://docs.microsoft.com/en-us/powershell/module/az.migrate/get-azmigratereplicationfabric
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Migrate/help/Get-AzMigrateReplicationFabric.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Migrate/help/Get-AzMigrateReplicationFabric.md
ms.openlocfilehash: 8230056069668765d3d27a9dd54538a310edf383
ms.sourcegitcommit: 68451baa389791703e666d95469602c5652609ee
ms.translationtype: MT
ms.contentlocale: sv-SE
ms.lasthandoff: 01/05/2021
ms.locfileid: "98522552"
---
# <span data-ttu-id="c36a1-101">Get-AzMigrateReplicationFabric</span><span class="sxs-lookup"><span data-stu-id="c36a1-101">Get-AzMigrateReplicationFabric</span></span>

## <span data-ttu-id="c36a1-102">Sammanfattning</span><span class="sxs-lookup"><span data-stu-id="c36a1-102">SYNOPSIS</span></span>
<span data-ttu-id="c36a1-103">Hämtar information om en Azure Site Recovery-Fabric.</span><span class="sxs-lookup"><span data-stu-id="c36a1-103">Gets the details of an Azure Site Recovery fabric.</span></span>

## <span data-ttu-id="c36a1-104">FRÅGESYNTAXEN</span><span class="sxs-lookup"><span data-stu-id="c36a1-104">SYNTAX</span></span>

### <span data-ttu-id="c36a1-105">Lista (standard)</span><span class="sxs-lookup"><span data-stu-id="c36a1-105">List (Default)</span></span>
```
Get-AzMigrateReplicationFabric -ResourceGroupName <String> -ResourceName <String> [-SubscriptionId <String[]>]
 [-DefaultProfile <PSObject>] [<CommonParameters>]
```

### <span data-ttu-id="c36a1-106">Lära</span><span class="sxs-lookup"><span data-stu-id="c36a1-106">Get</span></span>
```
Get-AzMigrateReplicationFabric -FabricName <String> -ResourceGroupName <String> -ResourceName <String>
 [-SubscriptionId <String[]>] [-DefaultProfile <PSObject>] [<CommonParameters>]
```

## <span data-ttu-id="c36a1-107">PROBLEMBESKRIVNING</span><span class="sxs-lookup"><span data-stu-id="c36a1-107">DESCRIPTION</span></span>
<span data-ttu-id="c36a1-108">Hämtar information om en Azure Site Recovery-Fabric.</span><span class="sxs-lookup"><span data-stu-id="c36a1-108">Gets the details of an Azure Site Recovery fabric.</span></span>

## <span data-ttu-id="c36a1-109">BESKRIVS</span><span class="sxs-lookup"><span data-stu-id="c36a1-109">EXAMPLES</span></span>

### <span data-ttu-id="c36a1-110">Exempel 1: Hämta alla Fabric efter resurs grupp och valv namn</span><span class="sxs-lookup"><span data-stu-id="c36a1-110">Example 1: Get all fabrics by resource group and vault name</span></span>
```powershell
PS C:\> PS Get-AzMigrateReplicationFabric -ResourceGroupName azmigratepwshtestasr13072020 -ResourceName AzMigrateTestProjectPWSH02aarsvault -FabricName AzMigratePWSHTc8d1replicationfabric

BcdrState                                 : Valid
CustomDetailInstanceType                  : VMwareV2
EncryptionDetailKekCertExpiryDate         :
EncryptionDetailKekCertThumbprint         :
EncryptionDetailKekState                  : None
FriendlyName                              : AzMigratePWSHTc8d1replicationfabric
Health                                    : Normal
HealthErrorDetail                         : {}
Id                                        : /Subscriptions/xxx-xxx-xxx/resourceGroups/azmigratepwshtestasr13072020/providers/Microsof
                                            t.RecoveryServices/vaults/AzMigrateTestProjectPWSH02aarsvault/replicationFabrics/AzMigratePWSHTc8d1replicationfabr
                                            ic
InternalIdentifier                        : 501ff8f2-c9d7-5bf4-87ff-d0b3fc98aeb5
Location                                  :
Name                                      : AzMigratePWSHTc8d1replicationfabric
RolloverEncryptionDetailKekCertExpiryDate :
RolloverEncryptionDetailKekCertThumbprint :
RolloverEncryptionDetailKekState          : None
Type                                      : Microsoft.RecoveryServices/vaults/replicationFabrics
```

<span data-ttu-id="c36a1-111">Skaffa alla Fabric i resurs gruppen och valvet</span><span class="sxs-lookup"><span data-stu-id="c36a1-111">Get all fabrics in resource group and vault</span></span>

### <span data-ttu-id="c36a1-112">Exempel 2: Hämta infrastruktur resurs grupp, valv namn och infrastruktur namn</span><span class="sxs-lookup"><span data-stu-id="c36a1-112">Example 2: Get fabric by resource group, vault name and fabric name</span></span>
```powershell
PS C:\> Get-AzMigrateReplicationFabric -ResourceGroupName azmigratepwshtestasr13072020 -ResourceName AzMigrateTestProjectPWSH02aarsvault

BcdrState                                 : Valid
CustomDetailInstanceType                  : VMwareV2
EncryptionDetailKekCertExpiryDate         :
EncryptionDetailKekCertThumbprint         :
EncryptionDetailKekState                  : None
FriendlyName                              : AzMigratePWSHTc8d1replicationfabric
Health                                    : Normal
HealthErrorDetail                         : {}
Id                                        : /Subscriptions/xxx-xxx-xxx/resourceGroups/azmigratepwshtestasr13072020/providers/Microsof
                                            t.RecoveryServices/vaults/AzMigrateTestProjectPWSH02aarsvault/replicationFabrics/AzMigratePWSHTc8d1replicationfabr
                                            ic
InternalIdentifier                        : 501ff8f2-c9d7-5bf4-87ff-d0b3fc98aeb5
Location                                  :
Name                                      : AzMigratePWSHTc8d1replicationfabric
RolloverEncryptionDetailKekCertExpiryDate :
RolloverEncryptionDetailKekCertThumbprint :
RolloverEncryptionDetailKekState          : None
Type                                      : Microsoft.RecoveryServices/vaults/replicationFabrics
```

<span data-ttu-id="c36a1-113">Skaffa en specifik infrastruktur resurs</span><span class="sxs-lookup"><span data-stu-id="c36a1-113">Get a specific fabric</span></span>

## <span data-ttu-id="c36a1-114">MALLPARAMETRAR</span><span class="sxs-lookup"><span data-stu-id="c36a1-114">PARAMETERS</span></span>

### <span data-ttu-id="c36a1-115">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="c36a1-115">-DefaultProfile</span></span>
<span data-ttu-id="c36a1-116">Autentiseringsuppgifter, konto, klient organisation och abonnemang som används för kommunikation med Azure.</span><span class="sxs-lookup"><span data-stu-id="c36a1-116">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="c36a1-117">-FabricName</span><span class="sxs-lookup"><span data-stu-id="c36a1-117">-FabricName</span></span>
<span data-ttu-id="c36a1-118">Fabric-namn.</span><span class="sxs-lookup"><span data-stu-id="c36a1-118">Fabric name.</span></span>

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

### <span data-ttu-id="c36a1-119">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="c36a1-119">-ResourceGroupName</span></span>
<span data-ttu-id="c36a1-120">Namnet på resurs gruppen där Recovery Services-valvet finns.</span><span class="sxs-lookup"><span data-stu-id="c36a1-120">The name of the resource group where the recovery services vault is present.</span></span>

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

### <span data-ttu-id="c36a1-121">-ResourceName</span><span class="sxs-lookup"><span data-stu-id="c36a1-121">-ResourceName</span></span>
<span data-ttu-id="c36a1-122">Namnet på Recovery Services-valvet.</span><span class="sxs-lookup"><span data-stu-id="c36a1-122">The name of the recovery services vault.</span></span>

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

### <span data-ttu-id="c36a1-123">-SubscriptionId</span><span class="sxs-lookup"><span data-stu-id="c36a1-123">-SubscriptionId</span></span>
<span data-ttu-id="c36a1-124">Abonnemangs-ID.</span><span class="sxs-lookup"><span data-stu-id="c36a1-124">The subscription Id.</span></span>

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

### <span data-ttu-id="c36a1-125">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="c36a1-125">CommonParameters</span></span>
<span data-ttu-id="c36a1-126">Den här cmdleten har stöd för de gemensamma parametrarna:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-disvariable,-utbuffer,-PipelineVariable,-verbose,-WarningAction och-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="c36a1-126">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="c36a1-127">Mer information finns i [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="c36a1-127">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="c36a1-128">KOSTNADS</span><span class="sxs-lookup"><span data-stu-id="c36a1-128">INPUTS</span></span>

## <span data-ttu-id="c36a1-129">VÄRDEN</span><span class="sxs-lookup"><span data-stu-id="c36a1-129">OUTPUTS</span></span>

### <span data-ttu-id="c36a1-130">Microsoft. Azure. PowerShell. cmdletar. Migrate. Models. Api20180110. IFabric</span><span class="sxs-lookup"><span data-stu-id="c36a1-130">Microsoft.Azure.PowerShell.Cmdlets.Migrate.Models.Api20180110.IFabric</span></span>

## <span data-ttu-id="c36a1-131">ANMÄRKNINGAR</span><span class="sxs-lookup"><span data-stu-id="c36a1-131">NOTES</span></span>

<span data-ttu-id="c36a1-132">ALIAS</span><span class="sxs-lookup"><span data-stu-id="c36a1-132">ALIASES</span></span>

## <span data-ttu-id="c36a1-133">RELATERADE LÄNKAR</span><span class="sxs-lookup"><span data-stu-id="c36a1-133">RELATED LINKS</span></span>

