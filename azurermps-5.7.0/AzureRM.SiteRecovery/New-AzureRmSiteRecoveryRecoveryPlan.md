---
external help file: Microsoft.Azure.Commands.SiteRecovery.dll-Help.xml
Module Name: AzureRM
ms.assetid: 1166EC21-5626-41F6-9CCE-2169CF202575
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.siterecovery/new-azurermsiterecoveryrecoveryplan
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/SiteRecovery/Commands.SiteRecovery/help/New-AzureRmSiteRecoveryRecoveryPlan.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/SiteRecovery/Commands.SiteRecovery/help/New-AzureRmSiteRecoveryRecoveryPlan.md
ms.openlocfilehash: 8aba5d85e11a6494c4362de4d729c5e7b64106fe
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: sv-SE
ms.lasthandoff: 08/20/2020
ms.locfileid: "93582952"
---
# <span data-ttu-id="c80c4-101">New-AzureRmSiteRecoveryRecoveryPlan</span><span class="sxs-lookup"><span data-stu-id="c80c4-101">New-AzureRmSiteRecoveryRecoveryPlan</span></span>

## <span data-ttu-id="c80c4-102">Sammanfattning</span><span class="sxs-lookup"><span data-stu-id="c80c4-102">SYNOPSIS</span></span>
<span data-ttu-id="c80c4-103">Skapar en plan för webbplats återställning i webbplats återställning.</span><span class="sxs-lookup"><span data-stu-id="c80c4-103">Creates a site recovery plan in Site Recovery.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="c80c4-104">FRÅGESYNTAXEN</span><span class="sxs-lookup"><span data-stu-id="c80c4-104">SYNTAX</span></span>

### <span data-ttu-id="c80c4-105">EnterpriseToEnterprise (standard)</span><span class="sxs-lookup"><span data-stu-id="c80c4-105">EnterpriseToEnterprise (Default)</span></span>
```
New-AzureRmSiteRecoveryRecoveryPlan -Name <String> -PrimaryFabric <ASRFabric> -RecoveryFabric <ASRFabric>
 -ReplicationProtectedItem <ASRReplicationProtectedItem[]> [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

### <span data-ttu-id="c80c4-106">EnterpriseToAzure</span><span class="sxs-lookup"><span data-stu-id="c80c4-106">EnterpriseToAzure</span></span>
```
New-AzureRmSiteRecoveryRecoveryPlan -Name <String> -PrimaryFabric <ASRFabric> [-Azure]
 -FailoverDeploymentModel <String> -ReplicationProtectedItem <ASRReplicationProtectedItem[]>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="c80c4-107">EnterpriseToEnterpriseLegacy</span><span class="sxs-lookup"><span data-stu-id="c80c4-107">EnterpriseToEnterpriseLegacy</span></span>
```
New-AzureRmSiteRecoveryRecoveryPlan -Name <String> -PrimaryServer <ASRServer> -RecoveryServer <ASRServer>
 -ProtectionEntityList <ASRProtectionEntity[]> [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="c80c4-108">EnterpriseToAzureLegacy</span><span class="sxs-lookup"><span data-stu-id="c80c4-108">EnterpriseToAzureLegacy</span></span>
```
New-AzureRmSiteRecoveryRecoveryPlan -Name <String> [-Azure] -FailoverDeploymentModel <String>
 -PrimaryServer <ASRServer> -ProtectionEntityList <ASRProtectionEntity[]>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="c80c4-109">HyperVSiteToAzureLegacy</span><span class="sxs-lookup"><span data-stu-id="c80c4-109">HyperVSiteToAzureLegacy</span></span>
```
New-AzureRmSiteRecoveryRecoveryPlan -Name <String> -FailoverDeploymentModel <String> -PrimarySite <ASRSite>
 -ProtectionEntityList <ASRProtectionEntity[]> [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="c80c4-110">ByRPFile</span><span class="sxs-lookup"><span data-stu-id="c80c4-110">ByRPFile</span></span>
```
New-AzureRmSiteRecoveryRecoveryPlan -Path <String> [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

## <span data-ttu-id="c80c4-111">PROBLEMBESKRIVNING</span><span class="sxs-lookup"><span data-stu-id="c80c4-111">DESCRIPTION</span></span>
<span data-ttu-id="c80c4-112">Cmdleten **New-AzureRmSiteRecoveryRecoveryPlan** skapar en återställnings plan i Azure Site Recovery.</span><span class="sxs-lookup"><span data-stu-id="c80c4-112">The **New-AzureRmSiteRecoveryRecoveryPlan** cmdlet creates a recovery plan in Azure Site Recovery.</span></span>

<span data-ttu-id="c80c4-113">En återställnings plan samlar virtuella datorer i en grupp för användning av redundans och återställning.</span><span class="sxs-lookup"><span data-stu-id="c80c4-113">A recovery plan gathers virtual machines in a group for the purposes of failover and recovery.</span></span>

## <span data-ttu-id="c80c4-114">BESKRIVS</span><span class="sxs-lookup"><span data-stu-id="c80c4-114">EXAMPLES</span></span>

### <span data-ttu-id="c80c4-115">Exempel 1: lägga till en återställnings plan i ett valv för webbplats återställning</span><span class="sxs-lookup"><span data-stu-id="c80c4-115">Example 1: Add a recovery plan to a Site Recovery vault</span></span>
```
PS C:\>New-AzureRmSiteRecoveryRecoveryPlan -Path "C:\Users\Contoso\Desktop\RecoveryPlan.xml"
```

<span data-ttu-id="c80c4-116">Det här kommandot lägger till återställnings planen RecoveryPlan.xml till Azure Site Recovery-valvet.</span><span class="sxs-lookup"><span data-stu-id="c80c4-116">This command adds the recovery plan named RecoveryPlan.xml to the Azure Site Recovery vault.</span></span>

## <span data-ttu-id="c80c4-117">MALLPARAMETRAR</span><span class="sxs-lookup"><span data-stu-id="c80c4-117">PARAMETERS</span></span>

### <span data-ttu-id="c80c4-118">-Azure</span><span class="sxs-lookup"><span data-stu-id="c80c4-118">-Azure</span></span>
```yaml
Type: SwitchParameter
Parameter Sets: EnterpriseToAzure, EnterpriseToAzureLegacy
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="c80c4-119">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="c80c4-119">-DefaultProfile</span></span>
<span data-ttu-id="c80c4-120">Autentiseringsuppgifter, konto, klient organisation och abonnemang som används för kommunikation med Azure.</span><span class="sxs-lookup"><span data-stu-id="c80c4-120">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

```yaml
Type: IAzureContextContainer
Parameter Sets: (All)
Aliases: AzureRmContext, AzureCredential

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="c80c4-121">-FailoverDeploymentModel</span><span class="sxs-lookup"><span data-stu-id="c80c4-121">-FailoverDeploymentModel</span></span>
```yaml
Type: String
Parameter Sets: EnterpriseToAzure, EnterpriseToAzureLegacy, HyperVSiteToAzureLegacy
Aliases: 
Accepted values: Classic, ResourceManager

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="c80c4-122">-Namn</span><span class="sxs-lookup"><span data-stu-id="c80c4-122">-Name</span></span>
```yaml
Type: String
Parameter Sets: EnterpriseToEnterprise, EnterpriseToAzure, EnterpriseToEnterpriseLegacy, EnterpriseToAzureLegacy, HyperVSiteToAzureLegacy
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="c80c4-123">-Path</span><span class="sxs-lookup"><span data-stu-id="c80c4-123">-Path</span></span>
<span data-ttu-id="c80c4-124">Anger sökvägen till återställnings plan filen.</span><span class="sxs-lookup"><span data-stu-id="c80c4-124">Specifies the path of the recovery plan file.</span></span>

```yaml
Type: String
Parameter Sets: ByRPFile
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="c80c4-125">-PrimaryFabric</span><span class="sxs-lookup"><span data-stu-id="c80c4-125">-PrimaryFabric</span></span>
```yaml
Type: ASRFabric
Parameter Sets: EnterpriseToEnterprise, EnterpriseToAzure
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="c80c4-126">-PrimaryServer</span><span class="sxs-lookup"><span data-stu-id="c80c4-126">-PrimaryServer</span></span>
```yaml
Type: ASRServer
Parameter Sets: EnterpriseToEnterpriseLegacy, EnterpriseToAzureLegacy
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="c80c4-127">-PrimarySite</span><span class="sxs-lookup"><span data-stu-id="c80c4-127">-PrimarySite</span></span>
```yaml
Type: ASRSite
Parameter Sets: HyperVSiteToAzureLegacy
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="c80c4-128">-ProtectionEntityList</span><span class="sxs-lookup"><span data-stu-id="c80c4-128">-ProtectionEntityList</span></span>
```yaml
Type: ASRProtectionEntity[]
Parameter Sets: EnterpriseToEnterpriseLegacy, EnterpriseToAzureLegacy, HyperVSiteToAzureLegacy
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="c80c4-129">-RecoveryFabric</span><span class="sxs-lookup"><span data-stu-id="c80c4-129">-RecoveryFabric</span></span>
```yaml
Type: ASRFabric
Parameter Sets: EnterpriseToEnterprise
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="c80c4-130">-RecoveryServer</span><span class="sxs-lookup"><span data-stu-id="c80c4-130">-RecoveryServer</span></span>
```yaml
Type: ASRServer
Parameter Sets: EnterpriseToEnterpriseLegacy
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="c80c4-131">-ReplicationProtectedItem</span><span class="sxs-lookup"><span data-stu-id="c80c4-131">-ReplicationProtectedItem</span></span>
```yaml
Type: ASRReplicationProtectedItem[]
Parameter Sets: EnterpriseToEnterprise, EnterpriseToAzure
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="c80c4-132">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="c80c4-132">CommonParameters</span></span>
<span data-ttu-id="c80c4-133">Den här cmdleten har stöd för de gemensamma parametrarna:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-disvariable,-utbuffer,-PipelineVariable,-verbose,-WarningAction och-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="c80c4-133">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="c80c4-134">Mer information finns i about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="c80c4-134">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="c80c4-135">KOSTNADS</span><span class="sxs-lookup"><span data-stu-id="c80c4-135">INPUTS</span></span>

### <span data-ttu-id="c80c4-136">ASRProtectionEntity[]</span><span class="sxs-lookup"><span data-stu-id="c80c4-136">ASRProtectionEntity[]</span></span>
<span data-ttu-id="c80c4-137">Parametern ' ProtectionEntityList ' godkänner värdet av typen ' ASRProtectionEntity [] ' från pipeline</span><span class="sxs-lookup"><span data-stu-id="c80c4-137">Parameter 'ProtectionEntityList' accepts value of type 'ASRProtectionEntity[]' from the pipeline</span></span>

### <span data-ttu-id="c80c4-138">ASRReplicationProtectedItem[]</span><span class="sxs-lookup"><span data-stu-id="c80c4-138">ASRReplicationProtectedItem[]</span></span>
<span data-ttu-id="c80c4-139">Parametern ' ReplicationProtectedItem ' godkänner värdet av typen ' ASRReplicationProtectedItem [] ' från pipeline</span><span class="sxs-lookup"><span data-stu-id="c80c4-139">Parameter 'ReplicationProtectedItem' accepts value of type 'ASRReplicationProtectedItem[]' from the pipeline</span></span>

## <span data-ttu-id="c80c4-140">VÄRDEN</span><span class="sxs-lookup"><span data-stu-id="c80c4-140">OUTPUTS</span></span>

## <span data-ttu-id="c80c4-141">ANMÄRKNINGAR</span><span class="sxs-lookup"><span data-stu-id="c80c4-141">NOTES</span></span>

## <span data-ttu-id="c80c4-142">RELATERADE LÄNKAR</span><span class="sxs-lookup"><span data-stu-id="c80c4-142">RELATED LINKS</span></span>

[<span data-ttu-id="c80c4-143">Get-AzureRmSiteRecoveryRecoveryPlan</span><span class="sxs-lookup"><span data-stu-id="c80c4-143">Get-AzureRmSiteRecoveryRecoveryPlan</span></span>](./Get-AzureRmSiteRecoveryRecoveryPlan.md)

[<span data-ttu-id="c80c4-144">Remove-AzureRmSiteRecoveryRecoveryPlan</span><span class="sxs-lookup"><span data-stu-id="c80c4-144">Remove-AzureRmSiteRecoveryRecoveryPlan</span></span>](./Remove-AzureRmSiteRecoveryRecoveryPlan.md)

[<span data-ttu-id="c80c4-145">Update-AzureRmSiteRecoveryRecoveryPlan</span><span class="sxs-lookup"><span data-stu-id="c80c4-145">Update-AzureRmSiteRecoveryRecoveryPlan</span></span>](./Update-AzureRmSiteRecoveryRecoveryPlan.md)


