---
external help file: Microsoft.Azure.PowerShell.Cmdlets.AnalysisServices.Dataplane.dll-Help.xml
Module Name: Az.AnalysisServices
online version: https://docs.microsoft.com/en-us/powershell/module/az.analysisservices/add-azanalysisservicesaccount
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/AnalysisServices/AnalysisServices/help/Add-AzAnalysisServicesAccount.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/AnalysisServices/AnalysisServices/help/Add-AzAnalysisServicesAccount.md
ms.openlocfilehash: f1d59a0a34072a91242c6595c269ba55c4397e0e
ms.sourcegitcommit: b4a38bcb0501a9016a4998efd377aa75d3ef9ce8
ms.translationtype: MT
ms.contentlocale: sv-SE
ms.lasthandoff: 10/27/2020
ms.locfileid: "94319732"
---
# <span data-ttu-id="7e13a-101">Add-AzAnalysisServicesAccount</span><span class="sxs-lookup"><span data-stu-id="7e13a-101">Add-AzAnalysisServicesAccount</span></span>

## <span data-ttu-id="7e13a-102">Sammanfattning</span><span class="sxs-lookup"><span data-stu-id="7e13a-102">SYNOPSIS</span></span>
<span data-ttu-id="7e13a-103">Lägger till ett autentiserat konto som ska användas för Azure Analysis Services server-cmdlet-begäranden.</span><span class="sxs-lookup"><span data-stu-id="7e13a-103">Adds an authenticated account to use for Azure Analysis Services server cmdlet requests.</span></span>

## <span data-ttu-id="7e13a-104">FRÅGESYNTAXEN</span><span class="sxs-lookup"><span data-stu-id="7e13a-104">SYNTAX</span></span>

### <span data-ttu-id="7e13a-105">UserParameterSetName (standard)</span><span class="sxs-lookup"><span data-stu-id="7e13a-105">UserParameterSetName (Default)</span></span>
```
Add-AzAnalysisServicesAccount [[-RolloutEnvironment] <String>] [[-Credential] <PSCredential>] [-WhatIf]
 [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="7e13a-106">ServicePrincipalWithPasswordParameterSetName</span><span class="sxs-lookup"><span data-stu-id="7e13a-106">ServicePrincipalWithPasswordParameterSetName</span></span>
```
Add-AzAnalysisServicesAccount [-RolloutEnvironment] <String> [-Credential] <PSCredential> [-ServicePrincipal]
 -TenantId <String> [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="7e13a-107">ServicePrincipalWithCertificateParameterSetName</span><span class="sxs-lookup"><span data-stu-id="7e13a-107">ServicePrincipalWithCertificateParameterSetName</span></span>
```
Add-AzAnalysisServicesAccount [-RolloutEnvironment] <String> [-ServicePrincipal] -TenantId <String>
 -ApplicationId <String> -CertificateThumbprint <String> [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="7e13a-108">PROBLEMBESKRIVNING</span><span class="sxs-lookup"><span data-stu-id="7e13a-108">DESCRIPTION</span></span>
<span data-ttu-id="7e13a-109">Add-AzAnalysisServicesAccount cmdlet används för att logga in på en instans av Azure Analysis Services-servern</span><span class="sxs-lookup"><span data-stu-id="7e13a-109">The Add-AzAnalysisServicesAccount cmdlet is used to login to an instance of Azure Analysis Services server</span></span>

## <span data-ttu-id="7e13a-110">BESKRIVS</span><span class="sxs-lookup"><span data-stu-id="7e13a-110">EXAMPLES</span></span>

### <span data-ttu-id="7e13a-111">Exempel 1</span><span class="sxs-lookup"><span data-stu-id="7e13a-111">Example 1</span></span>
```
PS C:\>Add-AzAnalysisServicesAccount
RolloutEnvironment: westcentralus.asazure.windows.net
Credential: $UserCredential
```

<span data-ttu-id="7e13a-112">I det här exemplet läggs det konto som anges i $UserCredential-variabel till Analysis Services-westcentralus.asazure.windows.net.</span><span class="sxs-lookup"><span data-stu-id="7e13a-112">This example will add the account specified by the $UserCredential variable to the westcentralus.asazure.windows.net Analysis Services environment.</span></span>

### <span data-ttu-id="7e13a-113">Exempel 2</span><span class="sxs-lookup"><span data-stu-id="7e13a-113">Example 2</span></span>
```
PS C:\>$ApplicationCredential = Get-Credential
PS C:\>Add-AzAnalysisServicesAccount -RolloutEnvironment 'westcentralus.asazure.windows.net' -ServicePrincipal -Credential $ApplicationCredential -TenantId "xxxx-xxxx-xxxx-xxxx"
```

<span data-ttu-id="7e13a-114">Det första kommandot får huvudautentiseringsuppgifter för program tjänsten och lagrar dem sedan i $ApplicationCredential variabel.</span><span class="sxs-lookup"><span data-stu-id="7e13a-114">The first command gets the application service principal credentials, and then stores them in the $ApplicationCredential variable.</span></span>
<span data-ttu-id="7e13a-115">Det andra kommandot lägger till det huvud konto för program tjänst som anges av $ApplicationCredential variabel och TenantId i westcentralus.asazure.windows.net Analysis Services Environment.</span><span class="sxs-lookup"><span data-stu-id="7e13a-115">The second command add the application service principal account specified by the $ApplicationCredential variable and TenantId to the westcentralus.asazure.windows.net Analysis Services environment.</span></span>

### <span data-ttu-id="7e13a-116">Exempel 3</span><span class="sxs-lookup"><span data-stu-id="7e13a-116">Example 3</span></span>
```
PS C:\>Add-AzAnalysisServicesAccount -RolloutEnvironment 'westcentralus.asazure.windows.net' -ServicePrincipal -ApplicationId "yyyy-yyyy-yyyy-yyyy" -CertificateThumbprint 'zzzzzzzzzzzzzzzz' -TenantId "xxxx-xxxx-xxxx-xxxx"
```

<span data-ttu-id="7e13a-117">I det här exemplet läggs huvud kontot för program tjänsten som anges av ApplicationId, TenantId och CertificateThumbprint till westcentralus.asazure.windows.net Analysis Services-miljön.</span><span class="sxs-lookup"><span data-stu-id="7e13a-117">This example will add the application service principal account specified by the ApplicationId, TenantId and CertificateThumbprint to the westcentralus.asazure.windows.net Analysis Services environment.</span></span>

## <span data-ttu-id="7e13a-118">MALLPARAMETRAR</span><span class="sxs-lookup"><span data-stu-id="7e13a-118">PARAMETERS</span></span>

### <span data-ttu-id="7e13a-119">-ApplicationId</span><span class="sxs-lookup"><span data-stu-id="7e13a-119">-ApplicationId</span></span>
<span data-ttu-id="7e13a-120">Program-ID.</span><span class="sxs-lookup"><span data-stu-id="7e13a-120">The application ID.</span></span>

```yaml
Type: System.String
Parameter Sets: ServicePrincipalWithCertificateParameterSetName
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="7e13a-121">-CertificateThumbprint</span><span class="sxs-lookup"><span data-stu-id="7e13a-121">-CertificateThumbprint</span></span>
<span data-ttu-id="7e13a-122">Certifikat-hash (tumavtryck)</span><span class="sxs-lookup"><span data-stu-id="7e13a-122">Certificate Hash (Thumbprint)</span></span>

```yaml
Type: System.String
Parameter Sets: ServicePrincipalWithCertificateParameterSetName
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="7e13a-123">-Autentiseringsuppgift</span><span class="sxs-lookup"><span data-stu-id="7e13a-123">-Credential</span></span>
<span data-ttu-id="7e13a-124">Inloggnings uppgifter</span><span class="sxs-lookup"><span data-stu-id="7e13a-124">Login credentials</span></span>

```yaml
Type: System.Management.Automation.PSCredential
Parameter Sets: UserParameterSetName
Aliases:

Required: False
Position: 1
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

```yaml
Type: System.Management.Automation.PSCredential
Parameter Sets: ServicePrincipalWithPasswordParameterSetName
Aliases:

Required: True
Position: 1
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="7e13a-125">-RolloutEnvironment</span><span class="sxs-lookup"><span data-stu-id="7e13a-125">-RolloutEnvironment</span></span>
<span data-ttu-id="7e13a-126">Namnet på Azure Analysis Services-miljön som du loggar in på.</span><span class="sxs-lookup"><span data-stu-id="7e13a-126">Name of the Azure Analysis Services environment to which to logon to.</span></span> <span data-ttu-id="7e13a-127">Givet det fullständiga namnet på servern till exempel asazure://westcentralus.asazure.windows.net/testserver, är det korrekta värdet för variabeln westcentralus.asazure.windows.net</span><span class="sxs-lookup"><span data-stu-id="7e13a-127">Given the full name of the server for example asazure://westcentralus.asazure.windows.net/testserver , the correct value for this variable will be westcentralus.asazure.windows.net</span></span>

```yaml
Type: System.String
Parameter Sets: UserParameterSetName
Aliases:

Required: False
Position: 0
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

```yaml
Type: System.String
Parameter Sets: ServicePrincipalWithPasswordParameterSetName, ServicePrincipalWithCertificateParameterSetName
Aliases:

Required: True
Position: 0
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="7e13a-128">-ServicePrincipal</span><span class="sxs-lookup"><span data-stu-id="7e13a-128">-ServicePrincipal</span></span>
<span data-ttu-id="7e13a-129">Anger att detta konto autentiserar genom att tillhandahålla tjänstens huvud referenser.</span><span class="sxs-lookup"><span data-stu-id="7e13a-129">Indicates that this account authenticates by providing service principal credentials.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: ServicePrincipalWithPasswordParameterSetName, ServicePrincipalWithCertificateParameterSetName
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="7e13a-130">-TenantId</span><span class="sxs-lookup"><span data-stu-id="7e13a-130">-TenantId</span></span>
<span data-ttu-id="7e13a-131">Klient organisationens namn eller ID</span><span class="sxs-lookup"><span data-stu-id="7e13a-131">Tenant name or ID</span></span>

```yaml
Type: System.String
Parameter Sets: ServicePrincipalWithPasswordParameterSetName, ServicePrincipalWithCertificateParameterSetName
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="7e13a-132">-Bekräfta</span><span class="sxs-lookup"><span data-stu-id="7e13a-132">-Confirm</span></span>
<span data-ttu-id="7e13a-133">Du uppmanas att bekräfta innan du kör cmdleten.</span><span class="sxs-lookup"><span data-stu-id="7e13a-133">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="7e13a-134">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="7e13a-134">-WhatIf</span></span>
<span data-ttu-id="7e13a-135">Visar vad som händer om cmdleten körs.</span><span class="sxs-lookup"><span data-stu-id="7e13a-135">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="7e13a-136">Cmdleten körs inte.</span><span class="sxs-lookup"><span data-stu-id="7e13a-136">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="7e13a-137">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="7e13a-137">CommonParameters</span></span>
<span data-ttu-id="7e13a-138">Den här cmdleten har stöd för de gemensamma parametrarna:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-disvariable,-utbuffer,-PipelineVariable,-verbose,-WarningAction och-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="7e13a-138">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="7e13a-139">Mer information finns i about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="7e13a-139">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="7e13a-140">KOSTNADS</span><span class="sxs-lookup"><span data-stu-id="7e13a-140">INPUTS</span></span>

### <span data-ttu-id="7e13a-141">Ingen</span><span class="sxs-lookup"><span data-stu-id="7e13a-141">None</span></span>

## <span data-ttu-id="7e13a-142">VÄRDEN</span><span class="sxs-lookup"><span data-stu-id="7e13a-142">OUTPUTS</span></span>

### <span data-ttu-id="7e13a-143">Microsoft. Azure. commands. AnalysisServices. Dataplane. AsAzureProfile</span><span class="sxs-lookup"><span data-stu-id="7e13a-143">Microsoft.Azure.Commands.AnalysisServices.Dataplane.AsAzureProfile</span></span>

## <span data-ttu-id="7e13a-144">ANMÄRKNINGAR</span><span class="sxs-lookup"><span data-stu-id="7e13a-144">NOTES</span></span>
<span data-ttu-id="7e13a-145">Alias: Login-AzAsAccount</span><span class="sxs-lookup"><span data-stu-id="7e13a-145">Alias: Login-AzAsAccount</span></span>

## <span data-ttu-id="7e13a-146">RELATERADE LÄNKAR</span><span class="sxs-lookup"><span data-stu-id="7e13a-146">RELATED LINKS</span></span>