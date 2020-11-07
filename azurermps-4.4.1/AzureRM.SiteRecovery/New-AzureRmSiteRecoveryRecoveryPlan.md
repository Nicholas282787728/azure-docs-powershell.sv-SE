---
external help file: Microsoft.Azure.Commands.SiteRecovery.dll-Help.xml
Module Name: AzureRM.SiteRecovery
ms.assetid: 1166EC21-5626-41F6-9CCE-2169CF202575
online version: ''
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/SiteRecovery/Commands.SiteRecovery/help/New-AzureRmSiteRecoveryRecoveryPlan.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/SiteRecovery/Commands.SiteRecovery/help/New-AzureRmSiteRecoveryRecoveryPlan.md
ms.openlocfilehash: fa308c0961d11320964d7c31a7d77642e968b09b
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: sv-SE
ms.lasthandoff: 08/20/2020
ms.locfileid: "93756547"
---
# <span data-ttu-id="9d80b-101">New-AzureRmSiteRecoveryRecoveryPlan</span><span class="sxs-lookup"><span data-stu-id="9d80b-101">New-AzureRmSiteRecoveryRecoveryPlan</span></span>

## <span data-ttu-id="9d80b-102">Sammanfattning</span><span class="sxs-lookup"><span data-stu-id="9d80b-102">SYNOPSIS</span></span>
<span data-ttu-id="9d80b-103">Skapar en plan för webbplats återställning i webbplats återställning.</span><span class="sxs-lookup"><span data-stu-id="9d80b-103">Creates a site recovery plan in Site Recovery.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="9d80b-104">FRÅGESYNTAXEN</span><span class="sxs-lookup"><span data-stu-id="9d80b-104">SYNTAX</span></span>

### <span data-ttu-id="9d80b-105">EnterpriseToEnterprise (standard)</span><span class="sxs-lookup"><span data-stu-id="9d80b-105">EnterpriseToEnterprise (Default)</span></span>
```
New-AzureRmSiteRecoveryRecoveryPlan -Name <String> -PrimaryFabric <ASRFabric> -RecoveryFabric <ASRFabric>
 -ReplicationProtectedItem <ASRReplicationProtectedItem[]> [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

### <span data-ttu-id="9d80b-106">EnterpriseToAzure</span><span class="sxs-lookup"><span data-stu-id="9d80b-106">EnterpriseToAzure</span></span>
```
New-AzureRmSiteRecoveryRecoveryPlan -Name <String> -PrimaryFabric <ASRFabric> [-Azure]
 -FailoverDeploymentModel <String> -ReplicationProtectedItem <ASRReplicationProtectedItem[]>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="9d80b-107">EnterpriseToEnterpriseLegacy</span><span class="sxs-lookup"><span data-stu-id="9d80b-107">EnterpriseToEnterpriseLegacy</span></span>
```
New-AzureRmSiteRecoveryRecoveryPlan -Name <String> -PrimaryServer <ASRServer> -RecoveryServer <ASRServer>
 -ProtectionEntityList <ASRProtectionEntity[]> [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="9d80b-108">EnterpriseToAzureLegacy</span><span class="sxs-lookup"><span data-stu-id="9d80b-108">EnterpriseToAzureLegacy</span></span>
```
New-AzureRmSiteRecoveryRecoveryPlan -Name <String> [-Azure] -FailoverDeploymentModel <String>
 -PrimaryServer <ASRServer> -ProtectionEntityList <ASRProtectionEntity[]>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="9d80b-109">HyperVSiteToAzureLegacy</span><span class="sxs-lookup"><span data-stu-id="9d80b-109">HyperVSiteToAzureLegacy</span></span>
```
New-AzureRmSiteRecoveryRecoveryPlan -Name <String> -FailoverDeploymentModel <String> -PrimarySite <ASRSite>
 -ProtectionEntityList <ASRProtectionEntity[]> [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="9d80b-110">ByRPFile</span><span class="sxs-lookup"><span data-stu-id="9d80b-110">ByRPFile</span></span>
```
New-AzureRmSiteRecoveryRecoveryPlan -Path <String> [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

## <span data-ttu-id="9d80b-111">PROBLEMBESKRIVNING</span><span class="sxs-lookup"><span data-stu-id="9d80b-111">DESCRIPTION</span></span>
<span data-ttu-id="9d80b-112">Cmdleten **New-AzureRmSiteRecoveryRecoveryPlan** skapar en återställnings plan i Azure Site Recovery.</span><span class="sxs-lookup"><span data-stu-id="9d80b-112">The **New-AzureRmSiteRecoveryRecoveryPlan** cmdlet creates a recovery plan in Azure Site Recovery.</span></span>

<span data-ttu-id="9d80b-113">En återställnings plan samlar virtuella datorer i en grupp för användning av redundans och återställning.</span><span class="sxs-lookup"><span data-stu-id="9d80b-113">A recovery plan gathers virtual machines in a group for the purposes of failover and recovery.</span></span>

## <span data-ttu-id="9d80b-114">BESKRIVS</span><span class="sxs-lookup"><span data-stu-id="9d80b-114">EXAMPLES</span></span>

### <span data-ttu-id="9d80b-115">Exempel 1: lägga till en återställnings plan i ett valv för webbplats återställning</span><span class="sxs-lookup"><span data-stu-id="9d80b-115">Example 1: Add a recovery plan to a Site Recovery vault</span></span>
```
PS C:\>New-AzureRmSiteRecoveryRecoveryPlan -Path "C:\Users\Contoso\Desktop\RecoveryPlan.xml"
```

<span data-ttu-id="9d80b-116">Det här kommandot lägger till återställnings planen RecoveryPlan.xml till Azure Site Recovery-valvet.</span><span class="sxs-lookup"><span data-stu-id="9d80b-116">This command adds the recovery plan named RecoveryPlan.xml to the Azure Site Recovery vault.</span></span>

## <span data-ttu-id="9d80b-117">MALLPARAMETRAR</span><span class="sxs-lookup"><span data-stu-id="9d80b-117">PARAMETERS</span></span>

### <span data-ttu-id="9d80b-118">-Azure</span><span class="sxs-lookup"><span data-stu-id="9d80b-118">-Azure</span></span>
```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: EnterpriseToAzure, EnterpriseToAzureLegacy
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="9d80b-119">-FailoverDeploymentModel</span><span class="sxs-lookup"><span data-stu-id="9d80b-119">-FailoverDeploymentModel</span></span>
```yaml
Type: System.String
Parameter Sets: EnterpriseToAzure, EnterpriseToAzureLegacy, HyperVSiteToAzureLegacy
Aliases: 
Accepted values: Classic, ResourceManager

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="9d80b-120">-Namn</span><span class="sxs-lookup"><span data-stu-id="9d80b-120">-Name</span></span>
```yaml
Type: System.String
Parameter Sets: EnterpriseToEnterprise, EnterpriseToAzure, EnterpriseToEnterpriseLegacy, EnterpriseToAzureLegacy, HyperVSiteToAzureLegacy
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="9d80b-121">-Path</span><span class="sxs-lookup"><span data-stu-id="9d80b-121">-Path</span></span>
<span data-ttu-id="9d80b-122">Anger sökvägen till återställnings plan filen.</span><span class="sxs-lookup"><span data-stu-id="9d80b-122">Specifies the path of the recovery plan file.</span></span>

```yaml
Type: System.String
Parameter Sets: ByRPFile
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="9d80b-123">-PrimaryFabric</span><span class="sxs-lookup"><span data-stu-id="9d80b-123">-PrimaryFabric</span></span>
```yaml
Type: Microsoft.Azure.Commands.SiteRecovery.ASRFabric
Parameter Sets: EnterpriseToEnterprise, EnterpriseToAzure
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="9d80b-124">-PrimaryServer</span><span class="sxs-lookup"><span data-stu-id="9d80b-124">-PrimaryServer</span></span>
```yaml
Type: Microsoft.Azure.Commands.SiteRecovery.ASRServer
Parameter Sets: EnterpriseToEnterpriseLegacy, EnterpriseToAzureLegacy
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="9d80b-125">-PrimarySite</span><span class="sxs-lookup"><span data-stu-id="9d80b-125">-PrimarySite</span></span>
```yaml
Type: Microsoft.Azure.Commands.SiteRecovery.ASRSite
Parameter Sets: HyperVSiteToAzureLegacy
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="9d80b-126">-ProtectionEntityList</span><span class="sxs-lookup"><span data-stu-id="9d80b-126">-ProtectionEntityList</span></span>
```yaml
Type: Microsoft.Azure.Commands.SiteRecovery.ASRProtectionEntity[]
Parameter Sets: EnterpriseToEnterpriseLegacy, EnterpriseToAzureLegacy, HyperVSiteToAzureLegacy
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="9d80b-127">-RecoveryFabric</span><span class="sxs-lookup"><span data-stu-id="9d80b-127">-RecoveryFabric</span></span>
```yaml
Type: Microsoft.Azure.Commands.SiteRecovery.ASRFabric
Parameter Sets: EnterpriseToEnterprise
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="9d80b-128">-RecoveryServer</span><span class="sxs-lookup"><span data-stu-id="9d80b-128">-RecoveryServer</span></span>
```yaml
Type: Microsoft.Azure.Commands.SiteRecovery.ASRServer
Parameter Sets: EnterpriseToEnterpriseLegacy
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="9d80b-129">-ReplicationProtectedItem</span><span class="sxs-lookup"><span data-stu-id="9d80b-129">-ReplicationProtectedItem</span></span>
```yaml
Type: Microsoft.Azure.Commands.SiteRecovery.ASRReplicationProtectedItem[]
Parameter Sets: EnterpriseToEnterprise, EnterpriseToAzure
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="9d80b-130">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="9d80b-130">-DefaultProfile</span></span>
<span data-ttu-id="9d80b-131">Autentiseringsuppgifter, konto, klient organisation och abonnemang som används för kommunikation med Azure.</span><span class="sxs-lookup"><span data-stu-id="9d80b-131">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

```yaml
Type: Microsoft.Azure.Commands.Common.Authentication.Abstractions.IAzureContextContainer
Parameter Sets: (All)
Aliases: AzureRmContext, AzureCredential

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="9d80b-132">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="9d80b-132">CommonParameters</span></span>
<span data-ttu-id="9d80b-133">Den här cmdleten har stöd för de gemensamma parametrarna:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-disvariable,-utbuffer,-PipelineVariable,-verbose,-WarningAction och-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="9d80b-133">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="9d80b-134">Mer information finns i about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="9d80b-134">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="9d80b-135">KOSTNADS</span><span class="sxs-lookup"><span data-stu-id="9d80b-135">INPUTS</span></span>

### <span data-ttu-id="9d80b-136">ASRProtectionEntity[]</span><span class="sxs-lookup"><span data-stu-id="9d80b-136">ASRProtectionEntity[]</span></span>
<span data-ttu-id="9d80b-137">Parametern ' ProtectionEntityList ' godkänner värdet av typen ' ASRProtectionEntity [] ' från pipeline</span><span class="sxs-lookup"><span data-stu-id="9d80b-137">Parameter 'ProtectionEntityList' accepts value of type 'ASRProtectionEntity[]' from the pipeline</span></span>

### <span data-ttu-id="9d80b-138">ASRReplicationProtectedItem[]</span><span class="sxs-lookup"><span data-stu-id="9d80b-138">ASRReplicationProtectedItem[]</span></span>
<span data-ttu-id="9d80b-139">Parametern ' ReplicationProtectedItem ' godkänner värdet av typen ' ASRReplicationProtectedItem [] ' från pipeline</span><span class="sxs-lookup"><span data-stu-id="9d80b-139">Parameter 'ReplicationProtectedItem' accepts value of type 'ASRReplicationProtectedItem[]' from the pipeline</span></span>

## <span data-ttu-id="9d80b-140">VÄRDEN</span><span class="sxs-lookup"><span data-stu-id="9d80b-140">OUTPUTS</span></span>

## <span data-ttu-id="9d80b-141">ANMÄRKNINGAR</span><span class="sxs-lookup"><span data-stu-id="9d80b-141">NOTES</span></span>

## <span data-ttu-id="9d80b-142">RELATERADE LÄNKAR</span><span class="sxs-lookup"><span data-stu-id="9d80b-142">RELATED LINKS</span></span>

[<span data-ttu-id="9d80b-143">Get-AzureRmSiteRecoveryRecoveryPlan</span><span class="sxs-lookup"><span data-stu-id="9d80b-143">Get-AzureRmSiteRecoveryRecoveryPlan</span></span>](./Get-AzureRmSiteRecoveryRecoveryPlan.md)

[<span data-ttu-id="9d80b-144">Remove-AzureRmSiteRecoveryRecoveryPlan</span><span class="sxs-lookup"><span data-stu-id="9d80b-144">Remove-AzureRmSiteRecoveryRecoveryPlan</span></span>](./Remove-AzureRmSiteRecoveryRecoveryPlan.md)

[<span data-ttu-id="9d80b-145">Update-AzureRmSiteRecoveryRecoveryPlan</span><span class="sxs-lookup"><span data-stu-id="9d80b-145">Update-AzureRmSiteRecoveryRecoveryPlan</span></span>](./Update-AzureRmSiteRecoveryRecoveryPlan.md)


