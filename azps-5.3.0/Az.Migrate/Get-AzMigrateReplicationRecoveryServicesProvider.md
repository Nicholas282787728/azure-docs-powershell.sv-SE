---
external help file: ''
Module Name: Az.Migrate
online version: https://docs.microsoft.com/en-us/powershell/module/az.migrate/get-azmigratereplicationrecoveryservicesprovider
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Migrate/help/Get-AzMigrateReplicationRecoveryServicesProvider.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Migrate/help/Get-AzMigrateReplicationRecoveryServicesProvider.md
ms.openlocfilehash: fd9bfed884ba2480a797ec5f83f99913496638e0
ms.sourcegitcommit: 68451baa389791703e666d95469602c5652609ee
ms.translationtype: MT
ms.contentlocale: sv-SE
ms.lasthandoff: 01/05/2021
ms.locfileid: "98521147"
---
# <span data-ttu-id="37abd-101">Get-AzMigrateReplicationRecoveryServicesProvider</span><span class="sxs-lookup"><span data-stu-id="37abd-101">Get-AzMigrateReplicationRecoveryServicesProvider</span></span>

## <span data-ttu-id="37abd-102">Sammanfattning</span><span class="sxs-lookup"><span data-stu-id="37abd-102">SYNOPSIS</span></span>
<span data-ttu-id="37abd-103">Hämtar information om registrerade Recovery Services-tjänster.</span><span class="sxs-lookup"><span data-stu-id="37abd-103">Gets the details of registered recovery services provider.</span></span>

## <span data-ttu-id="37abd-104">FRÅGESYNTAXEN</span><span class="sxs-lookup"><span data-stu-id="37abd-104">SYNTAX</span></span>

### <span data-ttu-id="37abd-105">Lista (standard)</span><span class="sxs-lookup"><span data-stu-id="37abd-105">List (Default)</span></span>
```
Get-AzMigrateReplicationRecoveryServicesProvider -ResourceGroupName <String> -ResourceName <String>
 [-SubscriptionId <String[]>] [-DefaultProfile <PSObject>] [<CommonParameters>]
```

### <span data-ttu-id="37abd-106">Lära</span><span class="sxs-lookup"><span data-stu-id="37abd-106">Get</span></span>
```
Get-AzMigrateReplicationRecoveryServicesProvider -FabricName <String> -ProviderName <String>
 -ResourceGroupName <String> -ResourceName <String> [-SubscriptionId <String[]>] [-DefaultProfile <PSObject>]
 [<CommonParameters>]
```

## <span data-ttu-id="37abd-107">PROBLEMBESKRIVNING</span><span class="sxs-lookup"><span data-stu-id="37abd-107">DESCRIPTION</span></span>
<span data-ttu-id="37abd-108">Hämtar information om registrerade Recovery Services-tjänster.</span><span class="sxs-lookup"><span data-stu-id="37abd-108">Gets the details of registered recovery services provider.</span></span>

## <span data-ttu-id="37abd-109">BESKRIVS</span><span class="sxs-lookup"><span data-stu-id="37abd-109">EXAMPLES</span></span>

### <span data-ttu-id="37abd-110">Exempel 1: Hämta alla providrar i valvet</span><span class="sxs-lookup"><span data-stu-id="37abd-110">Example 1: Get all providers in vault</span></span>
```powershell
PS C:\> Get-AzMigrateReplicationRecoveryServicesProvider -ResourceGroupName azmigratepwshtestasr13072020 -ResourceName AzMigrateTestProjectPWSH02aarsvault

Location Name                  Type
-------- ----                  ----
         AzMigratePWSHTc8d1dra Microsoft.RecoveryServices/vaults/replicationFabrics/replicationRecoveryServicesProviders
```

<span data-ttu-id="37abd-111">Visa alla.</span><span class="sxs-lookup"><span data-stu-id="37abd-111">List all.</span></span>

## <span data-ttu-id="37abd-112">MALLPARAMETRAR</span><span class="sxs-lookup"><span data-stu-id="37abd-112">PARAMETERS</span></span>

### <span data-ttu-id="37abd-113">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="37abd-113">-DefaultProfile</span></span>
<span data-ttu-id="37abd-114">Autentiseringsuppgifter, konto, klient organisation och abonnemang som används för kommunikation med Azure.</span><span class="sxs-lookup"><span data-stu-id="37abd-114">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="37abd-115">-FabricName</span><span class="sxs-lookup"><span data-stu-id="37abd-115">-FabricName</span></span>
<span data-ttu-id="37abd-116">Fabric-namn.</span><span class="sxs-lookup"><span data-stu-id="37abd-116">Fabric name.</span></span>

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

### <span data-ttu-id="37abd-117">-ProviderName</span><span class="sxs-lookup"><span data-stu-id="37abd-117">-ProviderName</span></span>
<span data-ttu-id="37abd-118">Leverantörs namn för Recovery Services</span><span class="sxs-lookup"><span data-stu-id="37abd-118">Recovery services provider name</span></span>

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

### <span data-ttu-id="37abd-119">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="37abd-119">-ResourceGroupName</span></span>
<span data-ttu-id="37abd-120">Namnet på resurs gruppen där Recovery Services-valvet finns.</span><span class="sxs-lookup"><span data-stu-id="37abd-120">The name of the resource group where the recovery services vault is present.</span></span>

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

### <span data-ttu-id="37abd-121">-ResourceName</span><span class="sxs-lookup"><span data-stu-id="37abd-121">-ResourceName</span></span>
<span data-ttu-id="37abd-122">Namnet på Recovery Services-valvet.</span><span class="sxs-lookup"><span data-stu-id="37abd-122">The name of the recovery services vault.</span></span>

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

### <span data-ttu-id="37abd-123">-SubscriptionId</span><span class="sxs-lookup"><span data-stu-id="37abd-123">-SubscriptionId</span></span>
<span data-ttu-id="37abd-124">Abonnemangs-ID.</span><span class="sxs-lookup"><span data-stu-id="37abd-124">The subscription Id.</span></span>

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

### <span data-ttu-id="37abd-125">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="37abd-125">CommonParameters</span></span>
<span data-ttu-id="37abd-126">Den här cmdleten har stöd för de gemensamma parametrarna:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-disvariable,-utbuffer,-PipelineVariable,-verbose,-WarningAction och-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="37abd-126">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="37abd-127">Mer information finns i [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="37abd-127">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="37abd-128">KOSTNADS</span><span class="sxs-lookup"><span data-stu-id="37abd-128">INPUTS</span></span>

## <span data-ttu-id="37abd-129">VÄRDEN</span><span class="sxs-lookup"><span data-stu-id="37abd-129">OUTPUTS</span></span>

### <span data-ttu-id="37abd-130">Microsoft. Azure. PowerShell. cmdletar. Migrate. Models. Api20180110. IRecoveryServicesProvider</span><span class="sxs-lookup"><span data-stu-id="37abd-130">Microsoft.Azure.PowerShell.Cmdlets.Migrate.Models.Api20180110.IRecoveryServicesProvider</span></span>

## <span data-ttu-id="37abd-131">ANMÄRKNINGAR</span><span class="sxs-lookup"><span data-stu-id="37abd-131">NOTES</span></span>

<span data-ttu-id="37abd-132">ALIAS</span><span class="sxs-lookup"><span data-stu-id="37abd-132">ALIASES</span></span>

## <span data-ttu-id="37abd-133">RELATERADE LÄNKAR</span><span class="sxs-lookup"><span data-stu-id="37abd-133">RELATED LINKS</span></span>

