---
external help file: Microsoft.Azure.Commands.Resources.dll-Help.xml
Module Name: AzureRM.Resources
ms.assetid: D602F910-B26F-473D-B5B6-C7BDFB0A14CB
online version: ''
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Resources/Commands.Resources/help/New-AzureRmADServicePrincipal.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Resources/Commands.Resources/help/New-AzureRmADServicePrincipal.md
ms.openlocfilehash: 4b327193a8dcbfecae8f13fa234da703d1a93cfb
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: sv-SE
ms.lasthandoff: 08/20/2020
ms.locfileid: "93758014"
---
# <span data-ttu-id="03646-101">New-AzureRmADServicePrincipal</span><span class="sxs-lookup"><span data-stu-id="03646-101">New-AzureRmADServicePrincipal</span></span>

## <span data-ttu-id="03646-102">Sammanfattning</span><span class="sxs-lookup"><span data-stu-id="03646-102">SYNOPSIS</span></span>
<span data-ttu-id="03646-103">Skapar ett nytt objekt i Azure Active Directory-tjänsten.</span><span class="sxs-lookup"><span data-stu-id="03646-103">Creates a new azure active directory service principal.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="03646-104">FRÅGESYNTAXEN</span><span class="sxs-lookup"><span data-stu-id="03646-104">SYNTAX</span></span>

### <span data-ttu-id="03646-105">ApplicationWithoutCredentialParameterSet (standard)</span><span class="sxs-lookup"><span data-stu-id="03646-105">ApplicationWithoutCredentialParameterSet (Default)</span></span>
```
New-AzureRmADServicePrincipal -ApplicationId <Guid> [-DefaultProfile <IAzureContextContainer>] [-WhatIf]
 [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="03646-106">ApplicationWithPasswordPlainParameterSet</span><span class="sxs-lookup"><span data-stu-id="03646-106">ApplicationWithPasswordPlainParameterSet</span></span>
```
New-AzureRmADServicePrincipal -ApplicationId <Guid> -Password <String> [-StartDate <DateTime>]
 [-EndDate <DateTime>] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="03646-107">ApplicationWithPasswordCredentialParameterSet</span><span class="sxs-lookup"><span data-stu-id="03646-107">ApplicationWithPasswordCredentialParameterSet</span></span>
```
New-AzureRmADServicePrincipal -ApplicationId <Guid> -PasswordCredentials <PSADPasswordCredential[]>
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="03646-108">ApplicationWithKeyPlainParameterSet</span><span class="sxs-lookup"><span data-stu-id="03646-108">ApplicationWithKeyPlainParameterSet</span></span>
```
New-AzureRmADServicePrincipal -ApplicationId <Guid> -CertValue <String> [-StartDate <DateTime>]
 [-EndDate <DateTime>] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="03646-109">ApplicationWithKeyCredentialParameterSet</span><span class="sxs-lookup"><span data-stu-id="03646-109">ApplicationWithKeyCredentialParameterSet</span></span>
```
New-AzureRmADServicePrincipal -ApplicationId <Guid> -KeyCredentials <PSADKeyCredential[]>
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="03646-110">DisplayNameWithoutCredentialParameterSet</span><span class="sxs-lookup"><span data-stu-id="03646-110">DisplayNameWithoutCredentialParameterSet</span></span>
```
New-AzureRmADServicePrincipal -DisplayName <String> [-DefaultProfile <IAzureContextContainer>] [-WhatIf]
 [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="03646-111">DisplayNameWithPasswordPlainParameterSet</span><span class="sxs-lookup"><span data-stu-id="03646-111">DisplayNameWithPasswordPlainParameterSet</span></span>
```
New-AzureRmADServicePrincipal -DisplayName <String> -Password <String> [-StartDate <DateTime>]
 [-EndDate <DateTime>] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="03646-112">DisplayNameWithPasswordCredentialParameterSet</span><span class="sxs-lookup"><span data-stu-id="03646-112">DisplayNameWithPasswordCredentialParameterSet</span></span>
```
New-AzureRmADServicePrincipal -DisplayName <String> -PasswordCredentials <PSADPasswordCredential[]>
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="03646-113">DisplayNameWithKeyPlainParameterSet</span><span class="sxs-lookup"><span data-stu-id="03646-113">DisplayNameWithKeyPlainParameterSet</span></span>
```
New-AzureRmADServicePrincipal -DisplayName <String> -CertValue <String> [-StartDate <DateTime>]
 [-EndDate <DateTime>] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="03646-114">DisplayNameWithKeyCredentialParameterSet</span><span class="sxs-lookup"><span data-stu-id="03646-114">DisplayNameWithKeyCredentialParameterSet</span></span>
```
New-AzureRmADServicePrincipal -DisplayName <String> -KeyCredentials <PSADKeyCredential[]>
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="03646-115">PROBLEMBESKRIVNING</span><span class="sxs-lookup"><span data-stu-id="03646-115">DESCRIPTION</span></span>
<span data-ttu-id="03646-116">Skapar ett nytt objekt i Azure Active Directory-tjänsten.</span><span class="sxs-lookup"><span data-stu-id="03646-116">Creates a new azure active directory service principal.</span></span>

<span data-ttu-id="03646-117">Obs! cmdleten skapar också implicit ett program och anger dess egenskaper (om ApplicationId inte finns).</span><span class="sxs-lookup"><span data-stu-id="03646-117">Note: The cmdlet also implicitly creates an application and sets its properties (if the ApplicationId is not provided).</span></span>
<span data-ttu-id="03646-118">Använd Set-AzureRmADApplication cmdlet för att uppdatera de programspecifika parametrarna.</span><span class="sxs-lookup"><span data-stu-id="03646-118">In order to update the application specific parameters please use Set-AzureRmADApplication cmdlet.</span></span>

## <span data-ttu-id="03646-119">BESKRIVS</span><span class="sxs-lookup"><span data-stu-id="03646-119">EXAMPLES</span></span>

### <span data-ttu-id="03646-120">--------------------------Exempel 1--------------------------</span><span class="sxs-lookup"><span data-stu-id="03646-120">--------------------------  Example 1  --------------------------</span></span>
```
New-AzureRmADServicePrincipal -ApplicationId 34a28ad2-dec4-4a41-bc3b-d22ddf90000e
```

<span data-ttu-id="03646-121">Skapar ett nytt objekt i Azure Active Directory-tjänsten.</span><span class="sxs-lookup"><span data-stu-id="03646-121">Creates a new azure active directory service principal.</span></span>

<span data-ttu-id="03646-122">DisplayName-typ ObjectId</span><span class="sxs-lookup"><span data-stu-id="03646-122">DisplayName                    Type                           ObjectId</span></span>
-----------                    ----                           --------
<span data-ttu-id="03646-123">DemoApp ServicePrincipal f95b6f5c-fc98-4af0-bb8a-34a14ca1dca1</span><span class="sxs-lookup"><span data-stu-id="03646-123">DemoApp                        ServicePrincipal               f95b6f5c-fc98-4af0-bb8a-34a14ca1dca1</span></span>

### <span data-ttu-id="03646-124">--------------------------Exempel 2--------------------------</span><span class="sxs-lookup"><span data-stu-id="03646-124">--------------------------  Example 2  --------------------------</span></span>
```
New-AzureRmADServicePrincipal -DisplayName SPForNoExistingApp
```

<span data-ttu-id="03646-125">Skapar ett nytt tjänst huvud.</span><span class="sxs-lookup"><span data-stu-id="03646-125">Creates a new service principal.</span></span>
<span data-ttu-id="03646-126">Cmdleten skapar också implicit ett program eftersom ett inte tillhandahålls.</span><span class="sxs-lookup"><span data-stu-id="03646-126">The cmdlet also implicitly creates an application since one is not provided.</span></span>

<span data-ttu-id="03646-127">DisplayName-typ ObjectId</span><span class="sxs-lookup"><span data-stu-id="03646-127">DisplayName                    Type                           ObjectId</span></span>
-----------                    ----                           --------
<span data-ttu-id="03646-128">SPForNoExistingApp ServicePrincipal 784136ca-3ae2-4fdd-a388-89d993e7c780</span><span class="sxs-lookup"><span data-stu-id="03646-128">SPForNoExistingApp             ServicePrincipal               784136ca-3ae2-4fdd-a388-89d993e7c780</span></span>

## <span data-ttu-id="03646-129">MALLPARAMETRAR</span><span class="sxs-lookup"><span data-stu-id="03646-129">PARAMETERS</span></span>

### <span data-ttu-id="03646-130">-ApplicationId</span><span class="sxs-lookup"><span data-stu-id="03646-130">-ApplicationId</span></span>
<span data-ttu-id="03646-131">Unikt program-ID för tjänstens huvud namn i en klient organisation.</span><span class="sxs-lookup"><span data-stu-id="03646-131">The unique application id for a service principal in a tenant.</span></span>
<span data-ttu-id="03646-132">Det går inte att ändra egenskapen när den har skapats.</span><span class="sxs-lookup"><span data-stu-id="03646-132">Once created this property cannot be changed.</span></span>
<span data-ttu-id="03646-133">Om inget program-ID anges genereras ett.</span><span class="sxs-lookup"><span data-stu-id="03646-133">If an application id is not specified, one will be generated.</span></span>

```yaml
Type: System.Guid
Parameter Sets: ApplicationWithoutCredentialParameterSet, ApplicationWithPasswordPlainParameterSet, ApplicationWithPasswordCredentialParameterSet, ApplicationWithKeyPlainParameterSet, ApplicationWithKeyCredentialParameterSet
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="03646-134">-CertValue</span><span class="sxs-lookup"><span data-stu-id="03646-134">-CertValue</span></span>
<span data-ttu-id="03646-135">Värdet för autentiseringstypen "asymmetrisk".</span><span class="sxs-lookup"><span data-stu-id="03646-135">The value of the "asymmetric" credential type.</span></span>
<span data-ttu-id="03646-136">Den representerar det grundläggande 64-kodade certifikatet.</span><span class="sxs-lookup"><span data-stu-id="03646-136">It represents the base 64 encoded certificate.</span></span>

```yaml
Type: System.String
Parameter Sets: ApplicationWithKeyPlainParameterSet, DisplayNameWithKeyPlainParameterSet
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="03646-137">-DisplayName</span><span class="sxs-lookup"><span data-stu-id="03646-137">-DisplayName</span></span>
<span data-ttu-id="03646-138">Eget namn på tjänstens huvud konto.</span><span class="sxs-lookup"><span data-stu-id="03646-138">The friendly name of the service principal.</span></span>

```yaml
Type: System.String
Parameter Sets: DisplayNameWithoutCredentialParameterSet, DisplayNameWithPasswordPlainParameterSet, DisplayNameWithPasswordCredentialParameterSet, DisplayNameWithKeyPlainParameterSet, DisplayNameWithKeyCredentialParameterSet
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="03646-139">-EndDate</span><span class="sxs-lookup"><span data-stu-id="03646-139">-EndDate</span></span>
<span data-ttu-id="03646-140">Slutdatum för användning av autentiseringsuppgifter.</span><span class="sxs-lookup"><span data-stu-id="03646-140">The effective end date of the credential usage.</span></span>
<span data-ttu-id="03646-141">Standardvärdet för slutdatumet är ett år från idag.</span><span class="sxs-lookup"><span data-stu-id="03646-141">The default end date value is one year from today.</span></span> <span data-ttu-id="03646-142">För en "asymmetrisk" typ autentiseringsuppgift måste detta ställas in på eller före det datum då X509-certifikatet är giltigt.</span><span class="sxs-lookup"><span data-stu-id="03646-142">For an "asymmetric" type credential, this must be set to on or before the date that the X509 certificate is valid.</span></span>

```yaml
Type: System.DateTime
Parameter Sets: ApplicationWithPasswordPlainParameterSet, ApplicationWithKeyPlainParameterSet, DisplayNameWithPasswordPlainParameterSet, DisplayNameWithKeyPlainParameterSet
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="03646-143">-Inloggnings uppgifter</span><span class="sxs-lookup"><span data-stu-id="03646-143">-KeyCredentials</span></span>
<span data-ttu-id="03646-144">Listan med autentiseringsuppgifter för certifikat som är kopplade till tjänstens huvud namn.</span><span class="sxs-lookup"><span data-stu-id="03646-144">The list of certificate credentials associated with the service principal.</span></span>

```yaml
Type: Microsoft.Azure.Graph.RBAC.Version1_6.ActiveDirectory.PSADKeyCredential[]
Parameter Sets: ApplicationWithKeyCredentialParameterSet, DisplayNameWithKeyCredentialParameterSet
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="03646-145">-Lösen ord</span><span class="sxs-lookup"><span data-stu-id="03646-145">-Password</span></span>
<span data-ttu-id="03646-146">Lösen ordet som ska kopplas till tjänstens huvud namn.</span><span class="sxs-lookup"><span data-stu-id="03646-146">The password to be associated with the service principal.</span></span>

```yaml
Type: System.String
Parameter Sets: ApplicationWithPasswordPlainParameterSet, DisplayNameWithPasswordPlainParameterSet
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="03646-147">-PasswordCredentials</span><span class="sxs-lookup"><span data-stu-id="03646-147">-PasswordCredentials</span></span>
<span data-ttu-id="03646-148">Listan med autentiseringsuppgifter för lösen ord som är kopplade till tjänstens huvud namn.</span><span class="sxs-lookup"><span data-stu-id="03646-148">The list of password credentials associated with the service principal.</span></span>

```yaml
Type: Microsoft.Azure.Graph.RBAC.Version1_6.ActiveDirectory.PSADPasswordCredential[]
Parameter Sets: ApplicationWithPasswordCredentialParameterSet, DisplayNameWithPasswordCredentialParameterSet
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="03646-149">-StartDate</span><span class="sxs-lookup"><span data-stu-id="03646-149">-StartDate</span></span>
<span data-ttu-id="03646-150">Start datum för användning av autentiseringsuppgifter.</span><span class="sxs-lookup"><span data-stu-id="03646-150">The effective start date of the credential usage.</span></span>
<span data-ttu-id="03646-151">Standardvärdet för start datum är idag.</span><span class="sxs-lookup"><span data-stu-id="03646-151">The default start date value is today.</span></span> <span data-ttu-id="03646-152">För en "asymmetrisk" typ autentiseringsuppgift måste detta ställas in på eller efter det datum då X509-certifikatet är giltigt från.</span><span class="sxs-lookup"><span data-stu-id="03646-152">For an "asymmetric" type credential, this must be set to on or after the date that the X509 certificate is valid from.</span></span>

```yaml
Type: System.DateTime
Parameter Sets: ApplicationWithPasswordPlainParameterSet, ApplicationWithKeyPlainParameterSet, DisplayNameWithPasswordPlainParameterSet, DisplayNameWithKeyPlainParameterSet
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="03646-153">-Bekräfta</span><span class="sxs-lookup"><span data-stu-id="03646-153">-Confirm</span></span>
<span data-ttu-id="03646-154">Du uppmanas att bekräfta innan du kör cmdleten.</span><span class="sxs-lookup"><span data-stu-id="03646-154">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="03646-155">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="03646-155">-WhatIf</span></span>
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

### <span data-ttu-id="03646-156">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="03646-156">-DefaultProfile</span></span>
<span data-ttu-id="03646-157">Autentiseringsuppgifter, konto, klient organisation och abonnemang som används för kommunikation med Azure.</span><span class="sxs-lookup"><span data-stu-id="03646-157">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="03646-158">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="03646-158">CommonParameters</span></span>
<span data-ttu-id="03646-159">Den här cmdleten har stöd för de gemensamma parametrarna:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-disvariable,-utbuffer,-PipelineVariable,-verbose,-WarningAction och-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="03646-159">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="03646-160">Mer information finns i about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="03646-160">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="03646-161">KOSTNADS</span><span class="sxs-lookup"><span data-stu-id="03646-161">INPUTS</span></span>

## <span data-ttu-id="03646-162">VÄRDEN</span><span class="sxs-lookup"><span data-stu-id="03646-162">OUTPUTS</span></span>

### <span data-ttu-id="03646-163">Microsoft.Azure.Graph.RBAC.Version1_6. ActiveDirectory. PSADServicePrincipal</span><span class="sxs-lookup"><span data-stu-id="03646-163">Microsoft.Azure.Graph.RBAC.Version1_6.ActiveDirectory.PSADServicePrincipal</span></span>

## <span data-ttu-id="03646-164">ANMÄRKNINGAR</span><span class="sxs-lookup"><span data-stu-id="03646-164">NOTES</span></span>
<span data-ttu-id="03646-165">Nyckelord: Azure, azurerm, arm, resurs, hantering, chef, resurs, grupp, Mall, distribution</span><span class="sxs-lookup"><span data-stu-id="03646-165">Keywords: azure, azurerm, arm, resource, management, manager, resource, group, template, deployment</span></span>

## <span data-ttu-id="03646-166">RELATERADE LÄNKAR</span><span class="sxs-lookup"><span data-stu-id="03646-166">RELATED LINKS</span></span>

[<span data-ttu-id="03646-167">Remove-AzureRmADServicePrincipal</span><span class="sxs-lookup"><span data-stu-id="03646-167">Remove-AzureRmADServicePrincipal</span></span>](./Remove-AzureRmADServicePrincipal.md)

[<span data-ttu-id="03646-168">Get-AzureRmADServicePrincipal</span><span class="sxs-lookup"><span data-stu-id="03646-168">Get-AzureRmADServicePrincipal</span></span>](./Get-AzureRmADServicePrincipal.md)

[<span data-ttu-id="03646-169">New-AzureRmADApplication</span><span class="sxs-lookup"><span data-stu-id="03646-169">New-AzureRmADApplication</span></span>](./New-AzureRmADApplication.md)

[<span data-ttu-id="03646-170">Remove-AzureRmADApplication</span><span class="sxs-lookup"><span data-stu-id="03646-170">Remove-AzureRmADApplication</span></span>](./Remove-AzureRmADApplication.md)

[<span data-ttu-id="03646-171">Get-AzureRmADSpCredential</span><span class="sxs-lookup"><span data-stu-id="03646-171">Get-AzureRmADSpCredential</span></span>](./Get-AzureRmADSpCredential.md)

[<span data-ttu-id="03646-172">New-AzureRmADSpCredential</span><span class="sxs-lookup"><span data-stu-id="03646-172">New-AzureRmADSpCredential</span></span>](./New-AzureRmADSpCredential.md)

[<span data-ttu-id="03646-173">Remove-AzureRmADSpCredential</span><span class="sxs-lookup"><span data-stu-id="03646-173">Remove-AzureRmADSpCredential</span></span>](./Remove-AzureRmADSpCredential.md)

