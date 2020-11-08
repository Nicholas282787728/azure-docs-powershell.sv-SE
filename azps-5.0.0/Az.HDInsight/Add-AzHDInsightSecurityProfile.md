---
external help file: Microsoft.Azure.PowerShell.Cmdlets.HDInsight.dll-Help.xml
Module Name: Az.HDInsight
ms.assetid: FB37494B-4035-45B7-88AB-DF33CEEF0D0A
online version: https://docs.microsoft.com/en-us/powershell/module/az.hdinsight/add-azhdinsightsecurityprofile
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/HDInsight/HDInsight/help/Add-AzHDInsightSecurityProfile.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/HDInsight/HDInsight/help/Add-AzHDInsightSecurityProfile.md
ms.openlocfilehash: c44fea946f98c6ac19e77e7012910afac37bff7c
ms.sourcegitcommit: b4a38bcb0501a9016a4998efd377aa75d3ef9ce8
ms.translationtype: MT
ms.contentlocale: sv-SE
ms.lasthandoff: 10/27/2020
ms.locfileid: "94263110"
---
# <span data-ttu-id="6cf78-101">Add-AzHDInsightSecurityProfile</span><span class="sxs-lookup"><span data-stu-id="6cf78-101">Add-AzHDInsightSecurityProfile</span></span>

## <span data-ttu-id="6cf78-102">Sammanfattning</span><span class="sxs-lookup"><span data-stu-id="6cf78-102">SYNOPSIS</span></span>
<span data-ttu-id="6cf78-103">Lägger till en säkerhets profil till ett kluster konfigurations objekt.</span><span class="sxs-lookup"><span data-stu-id="6cf78-103">Adds a security profile to a cluster configuration object.</span></span>

## <span data-ttu-id="6cf78-104">FRÅGESYNTAXEN</span><span class="sxs-lookup"><span data-stu-id="6cf78-104">SYNTAX</span></span>

```
Add-AzHDInsightSecurityProfile [-Config] <AzureHDInsightConfig> -DomainResourceId <String>
 -DomainUserCredential <PSCredential> [-OrganizationalUnitDN <String>] -LdapsUrls <String[]>
 [-ClusterUsersGroupDNs <String[]>] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

## <span data-ttu-id="6cf78-105">PROBLEMBESKRIVNING</span><span class="sxs-lookup"><span data-stu-id="6cf78-105">DESCRIPTION</span></span>
<span data-ttu-id="6cf78-106">Säkerhets profil används för att skapa ett säkert kluster genom att kerberizing det.</span><span class="sxs-lookup"><span data-stu-id="6cf78-106">Security profile is used to create a secure cluster by kerberizing it.</span></span>
<span data-ttu-id="6cf78-107">Säkerhets profilen innehåller konfiguration för att ansluta till klustret till Active Directory-domänen.</span><span class="sxs-lookup"><span data-stu-id="6cf78-107">Security profile contains configuration related joining the cluster to Active Directory Domain.</span></span>

## <span data-ttu-id="6cf78-108">BESKRIVS</span><span class="sxs-lookup"><span data-stu-id="6cf78-108">EXAMPLES</span></span>

### <span data-ttu-id="6cf78-109">Exempel 1: Lägg till säkerhets profil till klustrets konfigurations objekt</span><span class="sxs-lookup"><span data-stu-id="6cf78-109">Example 1: Add security profile to the cluster configuration object</span></span>
```
PS C:\> #Primary storage account info
PS C:\> $storageAccountResourceGroupName = "Group"
PS C:\> $storageAccountResourceId = "yourstorageaccountresourceid"
PS C:\> $storageAccountName = "yourstorageacct001"
PS C:\> $storageAccountKey = (Get-AzStorageAccountKey -ResourceGroupName $storageAccountResourceGroupName -Name $storageAccountName)[0].value

PS C:\> $storageContainer = "container001"

# Cluster configuration info
PS C:\> $location = "East US 2"
PS C:\> $clusterResourceGroupName = "Group"
PS C:\> $clusterName = "your-hadoop-001"
PS C:\> $clusterCreds = Get-Credential

# If the cluster's resource group doesn't exist yet, run:
#   New-AzResourceGroup -Name $clusterResourceGroupName -Location $location

#Security profile info
PS C:\> $domain="sampledomain.onmicrosoft.com"
PS C:\> $domainUser="sample.user@sampledomain.onmicrosoft.com"
PS C:\> $domainPassword=ConvertTo-SecureString "domainPassword" -AsPlainText -Force
PS C:\> $domainUserCredential=New-Object System.Management.Automation.PSCredential($domainUser, $domainPassword)
PS C:\> $organizationalUnitDN="ou=testunitdn"
PS C:\> $ldapsUrls=("ldaps://sampledomain.onmicrosoft.com:636","ldaps://sampledomain.onmicrosoft.com:389")
PS C:\> $clusterUsersGroupDNs=("groupdn1","groupdn2")

# Create the cluster
PS C:\> New-AzHDInsightClusterConfig `
            | Add-AzHDInsightSecurityProfile `
                -Domain $domain `
                -DomainUserCredential $domainUserCredential `
                -OrganizationalUnitDN $organizationalUnitDN `
                -LdapsUrls $ldapsUrls `
                -ClusterUsersGroupDNs $clusterUsersGroupDNs `
            | New-AzHDInsightCluster `
                -ClusterType Spark `
                -OSType Linux `
                -ClusterSizeInNodes 4 `
                -ResourceGroupName $clusterResourceGroupName `
                -ClusterName $clusterName `
                -HttpCredential $clusterCreds `
                -Location $location `
                -StorageAccountResourceId $storageAccountResourceId `
                -StorageAccountKey $storageAccountKey `
                -StorageContainer $storageContainer
```

<span data-ttu-id="6cf78-110">Det här kommandot lägger till ett säkerhets profil värde till det kluster som heter ditt-Hadoop-001.</span><span class="sxs-lookup"><span data-stu-id="6cf78-110">This command adds a security profile value to the cluster named your-hadoop-001.</span></span>

## <span data-ttu-id="6cf78-111">MALLPARAMETRAR</span><span class="sxs-lookup"><span data-stu-id="6cf78-111">PARAMETERS</span></span>

### <span data-ttu-id="6cf78-112">-ClusterUsersGroupDNs</span><span class="sxs-lookup"><span data-stu-id="6cf78-112">-ClusterUsersGroupDNs</span></span>
<span data-ttu-id="6cf78-113">Unika namn för Active Directory-grupper som är tillgängliga i Ambari och Ranger</span><span class="sxs-lookup"><span data-stu-id="6cf78-113">Distinguished names of the Active Directory groups that will be available in Ambari and Ranger</span></span>

```yaml
Type: System.String[]
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="6cf78-114">-Config</span><span class="sxs-lookup"><span data-stu-id="6cf78-114">-Config</span></span>
<span data-ttu-id="6cf78-115">Anger det HDInsight-kluster konfigurations objekt som denna cmdlet ändrar.</span><span class="sxs-lookup"><span data-stu-id="6cf78-115">Specifies the HDInsight cluster configuration object that this cmdlet modifies.</span></span>
<span data-ttu-id="6cf78-116">Det här objektet skapas av New-AzHDInsightClusterConfig cmdlet.</span><span class="sxs-lookup"><span data-stu-id="6cf78-116">This object is created by the New-AzHDInsightClusterConfig cmdlet.</span></span>

```yaml
Type: Microsoft.Azure.Commands.HDInsight.Models.AzureHDInsightConfig
Parameter Sets: (All)
Aliases:

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="6cf78-117">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="6cf78-117">-DefaultProfile</span></span>
<span data-ttu-id="6cf78-118">Autentiseringsuppgifter, konto, klient organisation och abonnemang som används för kommunikation med Azure</span><span class="sxs-lookup"><span data-stu-id="6cf78-118">The credentials, account, tenant, and subscription used for communication with azure</span></span>

```yaml
Type: Microsoft.Azure.Commands.Common.Authentication.Abstractions.Core.IAzureContextContainer
Parameter Sets: (All)
Aliases: AzContext, AzureRmContext, AzureCredential

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="6cf78-119">-DomainResourceId</span><span class="sxs-lookup"><span data-stu-id="6cf78-119">-DomainResourceId</span></span>
<span data-ttu-id="6cf78-120">Active Directory Domain Resource ID för klustret.</span><span class="sxs-lookup"><span data-stu-id="6cf78-120">Active Directory domain resource id for the cluster.</span></span>

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

### <span data-ttu-id="6cf78-121">-DomainUserCredential</span><span class="sxs-lookup"><span data-stu-id="6cf78-121">-DomainUserCredential</span></span>
<span data-ttu-id="6cf78-122">Ett domän användar konto uppgifter med tillräcklig behörighet för att skapa klustret.</span><span class="sxs-lookup"><span data-stu-id="6cf78-122">A domain user account credential with sufficient permissions for creating the cluster.</span></span>
<span data-ttu-id="6cf78-123">Användar namnet ska vara i user@domain format</span><span class="sxs-lookup"><span data-stu-id="6cf78-123">Username should be in user@domain format</span></span>

```yaml
Type: System.Management.Automation.PSCredential
Parameter Sets: (All)
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="6cf78-124">-LdapsUrls</span><span class="sxs-lookup"><span data-stu-id="6cf78-124">-LdapsUrls</span></span>
<span data-ttu-id="6cf78-125">URL: er för en eller flera LDAP-servrar för Active Directory</span><span class="sxs-lookup"><span data-stu-id="6cf78-125">Urls of one or multiple LDAPS servers for the Active Directory</span></span>

```yaml
Type: System.String[]
Parameter Sets: (All)
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="6cf78-126">-OrganizationalUnitDN</span><span class="sxs-lookup"><span data-stu-id="6cf78-126">-OrganizationalUnitDN</span></span>
<span data-ttu-id="6cf78-127">Unikt namn på organisationsenheten i Active Directory där användare och dator konton skapas</span><span class="sxs-lookup"><span data-stu-id="6cf78-127">Distinguished name of the organizational unit in the Active directory where user and computer accounts will be created</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="6cf78-128">-Bekräfta</span><span class="sxs-lookup"><span data-stu-id="6cf78-128">-Confirm</span></span>
<span data-ttu-id="6cf78-129">Du uppmanas att bekräfta innan du kör cmdleten.</span><span class="sxs-lookup"><span data-stu-id="6cf78-129">Prompts you for confirmation before running the cmdlet.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases: cf

Required: False
Position: Named
Default value: False
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="6cf78-130">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="6cf78-130">-WhatIf</span></span>
```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases: wi

Required: False
Position: Named
Default value: False
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="6cf78-131">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="6cf78-131">CommonParameters</span></span>
<span data-ttu-id="6cf78-132">Den här cmdleten har stöd för de gemensamma parametrarna:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-disvariable,-utbuffer,-PipelineVariable,-verbose,-WarningAction och-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="6cf78-132">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="6cf78-133">Mer information finns i [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="6cf78-133">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="6cf78-134">KOSTNADS</span><span class="sxs-lookup"><span data-stu-id="6cf78-134">INPUTS</span></span>

### <span data-ttu-id="6cf78-135">Microsoft. Azure. commands. HDInsight. Models. AzureHDInsightConfig</span><span class="sxs-lookup"><span data-stu-id="6cf78-135">Microsoft.Azure.Commands.HDInsight.Models.AzureHDInsightConfig</span></span>
## <span data-ttu-id="6cf78-136">VÄRDEN</span><span class="sxs-lookup"><span data-stu-id="6cf78-136">OUTPUTS</span></span>

### <span data-ttu-id="6cf78-137">Microsoft. Azure. commands. HDInsight. Models. AzureHDInsightSecurityProfile</span><span class="sxs-lookup"><span data-stu-id="6cf78-137">Microsoft.Azure.Commands.HDInsight.Models.AzureHDInsightSecurityProfile</span></span>
## <span data-ttu-id="6cf78-138">ANMÄRKNINGAR</span><span class="sxs-lookup"><span data-stu-id="6cf78-138">NOTES</span></span>

## <span data-ttu-id="6cf78-139">RELATERADE LÄNKAR</span><span class="sxs-lookup"><span data-stu-id="6cf78-139">RELATED LINKS</span></span>
