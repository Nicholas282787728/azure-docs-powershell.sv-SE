---
external help file: Microsoft.Azure.PowerShell.Cmdlets.HDInsight.dll-Help.xml
Module Name: Az.HDInsight
ms.assetid: FB37494B-4035-45B7-88AB-DF33CEEF0D0A
online version: https://docs.microsoft.com/en-us/powershell/module/az.hdinsight/add-azhdinsightsecurityprofile
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/HDInsight/HDInsight/help/Add-AzHDInsightSecurityProfile.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/HDInsight/HDInsight/help/Add-AzHDInsightSecurityProfile.md
ms.openlocfilehash: 712e3a6f90e37a38584ba27ab1ef07da019dc06a
ms.sourcegitcommit: 4d2c178cd6df9151877b08d54c1f4a228dbec9d1
ms.translationtype: MT
ms.contentlocale: sv-SE
ms.lasthandoff: 01/29/2020
ms.locfileid: "93916666"
---
# <span data-ttu-id="e818f-101">Add-AzHDInsightSecurityProfile</span><span class="sxs-lookup"><span data-stu-id="e818f-101">Add-AzHDInsightSecurityProfile</span></span>

## <span data-ttu-id="e818f-102">Sammanfattning</span><span class="sxs-lookup"><span data-stu-id="e818f-102">SYNOPSIS</span></span>
<span data-ttu-id="e818f-103">Lägger till ett säkerhets-ett kluster konfigurations objekt.</span><span class="sxs-lookup"><span data-stu-id="e818f-103">Adds a security profileto a cluster configuration object.</span></span>

## <span data-ttu-id="e818f-104">FRÅGESYNTAXEN</span><span class="sxs-lookup"><span data-stu-id="e818f-104">SYNTAX</span></span>

```
Add-AzHDInsightSecurityProfile [-Config] <AzureHDInsightConfig> -Domain <String>
 -DomainUserCredential <PSCredential> -OrganizationalUnitDN <String> -LdapsUrls <String[]>
 [-ClusterUsersGroupDNs <String[]>] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

## <span data-ttu-id="e818f-105">PROBLEMBESKRIVNING</span><span class="sxs-lookup"><span data-stu-id="e818f-105">DESCRIPTION</span></span>
<span data-ttu-id="e818f-106">Säkerhets profil används för att skapa ett säkert kluster genom att kerberizing det.</span><span class="sxs-lookup"><span data-stu-id="e818f-106">Security profile is used to create a secure cluster by kerberizing it.</span></span>
<span data-ttu-id="e818f-107">Säkerhets profilen innehåller konfiguration för att ansluta till klustret till Active Directory-domänen.</span><span class="sxs-lookup"><span data-stu-id="e818f-107">Security profile contains configuration related joining the cluster to Active Directory Domain.</span></span>

## <span data-ttu-id="e818f-108">BESKRIVS</span><span class="sxs-lookup"><span data-stu-id="e818f-108">EXAMPLES</span></span>

### <span data-ttu-id="e818f-109">Exempel 1</span><span class="sxs-lookup"><span data-stu-id="e818f-109">Example 1</span></span>
```
PS C:\> {{ Add example code here }}
```

<span data-ttu-id="e818f-110">{{Lägga till exempel beskrivning här}}</span><span class="sxs-lookup"><span data-stu-id="e818f-110">{{ Add example description here }}</span></span>

## <span data-ttu-id="e818f-111">MALLPARAMETRAR</span><span class="sxs-lookup"><span data-stu-id="e818f-111">PARAMETERS</span></span>

### <span data-ttu-id="e818f-112">-ClusterUsersGroupDNs</span><span class="sxs-lookup"><span data-stu-id="e818f-112">-ClusterUsersGroupDNs</span></span>
<span data-ttu-id="e818f-113">Unika namn för Active Directory-grupper som är tillgängliga i Ambari och Ranger</span><span class="sxs-lookup"><span data-stu-id="e818f-113">Distinguished names of the Active Directory groups that will be available in Ambari and Ranger</span></span>

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

### <span data-ttu-id="e818f-114">-Config</span><span class="sxs-lookup"><span data-stu-id="e818f-114">-Config</span></span>
<span data-ttu-id="e818f-115">Anger det HDInsight-kluster konfigurations objekt som denna cmdlet ändrar.</span><span class="sxs-lookup"><span data-stu-id="e818f-115">Specifies the HDInsight cluster configuration object that this cmdlet modifies.</span></span>
<span data-ttu-id="e818f-116">Det här objektet skapas av New-AzHDInsightClusterConfig cmdlet.</span><span class="sxs-lookup"><span data-stu-id="e818f-116">This object is created by the New-AzHDInsightClusterConfig cmdlet.</span></span>

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

### <span data-ttu-id="e818f-117">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="e818f-117">-DefaultProfile</span></span>
<span data-ttu-id="e818f-118">Autentiseringsuppgifter, konto, klient organisation och abonnemang som används för kommunikation med Azure</span><span class="sxs-lookup"><span data-stu-id="e818f-118">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="e818f-119">-Domain</span><span class="sxs-lookup"><span data-stu-id="e818f-119">-Domain</span></span>
<span data-ttu-id="e818f-120">Active Directory-domän för klustret</span><span class="sxs-lookup"><span data-stu-id="e818f-120">Active Directory domain for the cluster</span></span>

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

### <span data-ttu-id="e818f-121">-DomainUserCredential</span><span class="sxs-lookup"><span data-stu-id="e818f-121">-DomainUserCredential</span></span>
<span data-ttu-id="e818f-122">Ett domän användar konto uppgifter med tillräcklig behörighet för att skapa klustret.</span><span class="sxs-lookup"><span data-stu-id="e818f-122">A domain user account credential with sufficient permissions for creating the cluster.</span></span>
<span data-ttu-id="e818f-123">Användar namnet ska vara i user@domain format</span><span class="sxs-lookup"><span data-stu-id="e818f-123">Username should be in user@domain format</span></span>

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

### <span data-ttu-id="e818f-124">-LdapsUrls</span><span class="sxs-lookup"><span data-stu-id="e818f-124">-LdapsUrls</span></span>
<span data-ttu-id="e818f-125">URL: er för en eller flera LDAP-servrar för Active Directory</span><span class="sxs-lookup"><span data-stu-id="e818f-125">Urls of one or multiple LDAPS servers for the Active Directory</span></span>

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

### <span data-ttu-id="e818f-126">-OrganizationalUnitDN</span><span class="sxs-lookup"><span data-stu-id="e818f-126">-OrganizationalUnitDN</span></span>
<span data-ttu-id="e818f-127">Unikt namn på organisationsenheten i Active Directory där användare och dator konton skapas</span><span class="sxs-lookup"><span data-stu-id="e818f-127">Distinguished name of the organizational unit in the Active directory where user and computer accounts will be created</span></span>

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

### <span data-ttu-id="e818f-128">-Bekräfta</span><span class="sxs-lookup"><span data-stu-id="e818f-128">-Confirm</span></span>
<span data-ttu-id="e818f-129">Du uppmanas att bekräfta innan du kör cmdleten.</span><span class="sxs-lookup"><span data-stu-id="e818f-129">Prompts you for confirmation before running the cmdlet.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases: cf

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="e818f-130">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="e818f-130">-WhatIf</span></span>
```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases: wi

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="e818f-131">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="e818f-131">CommonParameters</span></span>
<span data-ttu-id="e818f-132">Den här cmdleten har stöd för de gemensamma parametrarna:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-disvariable,-utbuffer,-PipelineVariable,-verbose,-WarningAction och-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="e818f-132">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="e818f-133">Mer information finns i about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="e818f-133">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="e818f-134">KOSTNADS</span><span class="sxs-lookup"><span data-stu-id="e818f-134">INPUTS</span></span>

### <span data-ttu-id="e818f-135">Microsoft. Azure. commands. HDInsight. Models. AzureHDInsightConfig</span><span class="sxs-lookup"><span data-stu-id="e818f-135">Microsoft.Azure.Commands.HDInsight.Models.AzureHDInsightConfig</span></span>

## <span data-ttu-id="e818f-136">VÄRDEN</span><span class="sxs-lookup"><span data-stu-id="e818f-136">OUTPUTS</span></span>

### <span data-ttu-id="e818f-137">Microsoft. Azure. commands. HDInsight. Models. AzureHDInsightSecurityProfile</span><span class="sxs-lookup"><span data-stu-id="e818f-137">Microsoft.Azure.Commands.HDInsight.Models.AzureHDInsightSecurityProfile</span></span>

## <span data-ttu-id="e818f-138">ANMÄRKNINGAR</span><span class="sxs-lookup"><span data-stu-id="e818f-138">NOTES</span></span>

## <span data-ttu-id="e818f-139">RELATERADE LÄNKAR</span><span class="sxs-lookup"><span data-stu-id="e818f-139">RELATED LINKS</span></span>
