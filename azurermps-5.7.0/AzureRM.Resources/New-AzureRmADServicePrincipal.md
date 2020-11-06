---
external help file: Microsoft.Azure.Commands.Resources.dll-Help.xml
Module Name: AzureRM.Resources
ms.assetid: D602F910-B26F-473D-B5B6-C7BDFB0A14CB
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.resources/new-azurermadserviceprincipal
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Resources/Commands.Resources/help/New-AzureRmADServicePrincipal.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Resources/Commands.Resources/help/New-AzureRmADServicePrincipal.md
ms.openlocfilehash: ca338fd648010b9158a6bc308bb4dcb2f1c48317
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: sv-SE
ms.lasthandoff: 08/20/2020
ms.locfileid: "93580995"
---
# <span data-ttu-id="e5823-101">New-AzureRmADServicePrincipal</span><span class="sxs-lookup"><span data-stu-id="e5823-101">New-AzureRmADServicePrincipal</span></span>

## <span data-ttu-id="e5823-102">Sammanfattning</span><span class="sxs-lookup"><span data-stu-id="e5823-102">SYNOPSIS</span></span>
<span data-ttu-id="e5823-103">Skapar ett nytt objekt i Azure Active Directory-tjänsten.</span><span class="sxs-lookup"><span data-stu-id="e5823-103">Creates a new azure active directory service principal.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="e5823-104">FRÅGESYNTAXEN</span><span class="sxs-lookup"><span data-stu-id="e5823-104">SYNTAX</span></span>

### <span data-ttu-id="e5823-105">ApplicationWithoutCredentialParameterSet (standard)</span><span class="sxs-lookup"><span data-stu-id="e5823-105">ApplicationWithoutCredentialParameterSet (Default)</span></span>
```
New-AzureRmADServicePrincipal -ApplicationId <Guid> [-DefaultProfile <IAzureContextContainer>] [-WhatIf]
 [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="e5823-106">ApplicationWithPasswordPlainParameterSet</span><span class="sxs-lookup"><span data-stu-id="e5823-106">ApplicationWithPasswordPlainParameterSet</span></span>
```
New-AzureRmADServicePrincipal -ApplicationId <Guid> -Password <SecureString> [-StartDate <DateTime>]
 [-EndDate <DateTime>] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="e5823-107">ApplicationWithPasswordCredentialParameterSet</span><span class="sxs-lookup"><span data-stu-id="e5823-107">ApplicationWithPasswordCredentialParameterSet</span></span>
```
New-AzureRmADServicePrincipal -ApplicationId <Guid> -PasswordCredentials <PSADPasswordCredential[]>
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="e5823-108">ApplicationWithKeyPlainParameterSet</span><span class="sxs-lookup"><span data-stu-id="e5823-108">ApplicationWithKeyPlainParameterSet</span></span>
```
New-AzureRmADServicePrincipal -ApplicationId <Guid> -CertValue <String> [-StartDate <DateTime>]
 [-EndDate <DateTime>] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="e5823-109">ApplicationWithKeyCredentialParameterSet</span><span class="sxs-lookup"><span data-stu-id="e5823-109">ApplicationWithKeyCredentialParameterSet</span></span>
```
New-AzureRmADServicePrincipal -ApplicationId <Guid> -KeyCredentials <PSADKeyCredential[]>
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="e5823-110">DisplayNameWithoutCredentialParameterSet</span><span class="sxs-lookup"><span data-stu-id="e5823-110">DisplayNameWithoutCredentialParameterSet</span></span>
```
New-AzureRmADServicePrincipal -DisplayName <String> [-DefaultProfile <IAzureContextContainer>] [-WhatIf]
 [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="e5823-111">DisplayNameWithPasswordPlainParameterSet</span><span class="sxs-lookup"><span data-stu-id="e5823-111">DisplayNameWithPasswordPlainParameterSet</span></span>
```
New-AzureRmADServicePrincipal -DisplayName <String> -Password <SecureString> [-StartDate <DateTime>]
 [-EndDate <DateTime>] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="e5823-112">DisplayNameWithPasswordCredentialParameterSet</span><span class="sxs-lookup"><span data-stu-id="e5823-112">DisplayNameWithPasswordCredentialParameterSet</span></span>
```
New-AzureRmADServicePrincipal -DisplayName <String> -PasswordCredentials <PSADPasswordCredential[]>
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="e5823-113">DisplayNameWithKeyPlainParameterSet</span><span class="sxs-lookup"><span data-stu-id="e5823-113">DisplayNameWithKeyPlainParameterSet</span></span>
```
New-AzureRmADServicePrincipal -DisplayName <String> -CertValue <String> [-StartDate <DateTime>]
 [-EndDate <DateTime>] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="e5823-114">DisplayNameWithKeyCredentialParameterSet</span><span class="sxs-lookup"><span data-stu-id="e5823-114">DisplayNameWithKeyCredentialParameterSet</span></span>
```
New-AzureRmADServicePrincipal -DisplayName <String> -KeyCredentials <PSADKeyCredential[]>
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="e5823-115">PROBLEMBESKRIVNING</span><span class="sxs-lookup"><span data-stu-id="e5823-115">DESCRIPTION</span></span>
<span data-ttu-id="e5823-116">Skapar ett nytt objekt i Azure Active Directory-tjänsten.</span><span class="sxs-lookup"><span data-stu-id="e5823-116">Creates a new azure active directory service principal.</span></span>

<span data-ttu-id="e5823-117">Obs! cmdleten skapar också implicit ett program och anger dess egenskaper (om ApplicationId inte finns).</span><span class="sxs-lookup"><span data-stu-id="e5823-117">Note: The cmdlet also implicitly creates an application and sets its properties (if the ApplicationId is not provided).</span></span>
<span data-ttu-id="e5823-118">Använd Set-AzureRmADApplication cmdlet för att uppdatera de programspecifika parametrarna.</span><span class="sxs-lookup"><span data-stu-id="e5823-118">In order to update the application specific parameters please use Set-AzureRmADApplication cmdlet.</span></span>

## <span data-ttu-id="e5823-119">BESKRIVS</span><span class="sxs-lookup"><span data-stu-id="e5823-119">EXAMPLES</span></span>

### <span data-ttu-id="e5823-120">Exempel 1</span><span class="sxs-lookup"><span data-stu-id="e5823-120">Example 1</span></span>
```
New-AzureRmADServicePrincipal -ApplicationId 34a28ad2-dec4-4a41-bc3b-d22ddf90000e
```

<span data-ttu-id="e5823-121">Skapar ett nytt objekt i Azure Active Directory-tjänsten.</span><span class="sxs-lookup"><span data-stu-id="e5823-121">Creates a new azure active directory service principal.</span></span>

<span data-ttu-id="e5823-122">DisplayName-typ ObjectId</span><span class="sxs-lookup"><span data-stu-id="e5823-122">DisplayName                    Type                           ObjectId</span></span>
-----------                    ----                           --------
<span data-ttu-id="e5823-123">DemoApp ServicePrincipal f95b6f5c-fc98-4af0-bb8a-34a14ca1dca1</span><span class="sxs-lookup"><span data-stu-id="e5823-123">DemoApp                        ServicePrincipal               f95b6f5c-fc98-4af0-bb8a-34a14ca1dca1</span></span>

### <span data-ttu-id="e5823-124">Exempel 2</span><span class="sxs-lookup"><span data-stu-id="e5823-124">Example 2</span></span>
```
$SecureStringPassword = ConvertTo-SecureString -String "password" -AsPlainText -Force
New-AzureRmADServicePrincipal -DisplayName SPForNoExistingApp -Password $SecureStringPassword
```

<span data-ttu-id="e5823-125">Skapar ett nytt tjänst huvud.</span><span class="sxs-lookup"><span data-stu-id="e5823-125">Creates a new service principal.</span></span>
<span data-ttu-id="e5823-126">Cmdleten skapar också implicit ett program eftersom ett inte tillhandahålls.</span><span class="sxs-lookup"><span data-stu-id="e5823-126">The cmdlet also implicitly creates an application since one is not provided.</span></span>

<span data-ttu-id="e5823-127">DisplayName-typ ObjectId</span><span class="sxs-lookup"><span data-stu-id="e5823-127">DisplayName                    Type                           ObjectId</span></span>
-----------                    ----                           --------
<span data-ttu-id="e5823-128">SPForNoExistingApp ServicePrincipal 784136ca-3ae2-4fdd-a388-89d993e7c780</span><span class="sxs-lookup"><span data-stu-id="e5823-128">SPForNoExistingApp             ServicePrincipal               784136ca-3ae2-4fdd-a388-89d993e7c780</span></span>

## <span data-ttu-id="e5823-129">MALLPARAMETRAR</span><span class="sxs-lookup"><span data-stu-id="e5823-129">PARAMETERS</span></span>

### <span data-ttu-id="e5823-130">-ApplicationId</span><span class="sxs-lookup"><span data-stu-id="e5823-130">-ApplicationId</span></span>
<span data-ttu-id="e5823-131">Unikt program-ID för tjänstens huvud namn i en klient organisation.</span><span class="sxs-lookup"><span data-stu-id="e5823-131">The unique application id for a service principal in a tenant.</span></span>
<span data-ttu-id="e5823-132">Det går inte att ändra egenskapen när den har skapats.</span><span class="sxs-lookup"><span data-stu-id="e5823-132">Once created this property cannot be changed.</span></span>
<span data-ttu-id="e5823-133">Om inget program-ID anges genereras ett.</span><span class="sxs-lookup"><span data-stu-id="e5823-133">If an application id is not specified, one will be generated.</span></span>

```yaml
Type: Guid
Parameter Sets: ApplicationWithoutCredentialParameterSet, ApplicationWithPasswordPlainParameterSet, ApplicationWithPasswordCredentialParameterSet, ApplicationWithKeyPlainParameterSet, ApplicationWithKeyCredentialParameterSet
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="e5823-134">-CertValue</span><span class="sxs-lookup"><span data-stu-id="e5823-134">-CertValue</span></span>
<span data-ttu-id="e5823-135">Värdet för autentiseringstypen "asymmetrisk".</span><span class="sxs-lookup"><span data-stu-id="e5823-135">The value of the "asymmetric" credential type.</span></span>
<span data-ttu-id="e5823-136">Den representerar det grundläggande 64-kodade certifikatet.</span><span class="sxs-lookup"><span data-stu-id="e5823-136">It represents the base 64 encoded certificate.</span></span>

```yaml
Type: String
Parameter Sets: ApplicationWithKeyPlainParameterSet, DisplayNameWithKeyPlainParameterSet
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="e5823-137">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="e5823-137">-DefaultProfile</span></span>
<span data-ttu-id="e5823-138">Autentiseringsuppgifter, konto, klient organisation och abonnemang som används för kommunikation med Azure</span><span class="sxs-lookup"><span data-stu-id="e5823-138">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="e5823-139">-DisplayName</span><span class="sxs-lookup"><span data-stu-id="e5823-139">-DisplayName</span></span>
<span data-ttu-id="e5823-140">Eget namn på tjänstens huvud konto.</span><span class="sxs-lookup"><span data-stu-id="e5823-140">The friendly name of the service principal.</span></span>

```yaml
Type: String
Parameter Sets: DisplayNameWithoutCredentialParameterSet, DisplayNameWithPasswordPlainParameterSet, DisplayNameWithPasswordCredentialParameterSet, DisplayNameWithKeyPlainParameterSet, DisplayNameWithKeyCredentialParameterSet
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="e5823-141">-EndDate</span><span class="sxs-lookup"><span data-stu-id="e5823-141">-EndDate</span></span>
<span data-ttu-id="e5823-142">Slutdatum för användning av autentiseringsuppgifter.</span><span class="sxs-lookup"><span data-stu-id="e5823-142">The effective end date of the credential usage.</span></span>
<span data-ttu-id="e5823-143">Standardvärdet för slutdatumet är ett år från idag.</span><span class="sxs-lookup"><span data-stu-id="e5823-143">The default end date value is one year from today.</span></span> <span data-ttu-id="e5823-144">För en "asymmetrisk" typ autentiseringsuppgift måste detta ställas in på eller före det datum då X509-certifikatet är giltigt.</span><span class="sxs-lookup"><span data-stu-id="e5823-144">For an "asymmetric" type credential, this must be set to on or before the date that the X509 certificate is valid.</span></span>

```yaml
Type: DateTime
Parameter Sets: ApplicationWithPasswordPlainParameterSet, ApplicationWithKeyPlainParameterSet, DisplayNameWithPasswordPlainParameterSet, DisplayNameWithKeyPlainParameterSet
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="e5823-145">-Inloggnings uppgifter</span><span class="sxs-lookup"><span data-stu-id="e5823-145">-KeyCredentials</span></span>
<span data-ttu-id="e5823-146">Listan med autentiseringsuppgifter för certifikat som är kopplade till tjänstens huvud namn.</span><span class="sxs-lookup"><span data-stu-id="e5823-146">The list of certificate credentials associated with the service principal.</span></span>

```yaml
Type: PSADKeyCredential[]
Parameter Sets: ApplicationWithKeyCredentialParameterSet, DisplayNameWithKeyCredentialParameterSet
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="e5823-147">-Lösen ord</span><span class="sxs-lookup"><span data-stu-id="e5823-147">-Password</span></span>
<span data-ttu-id="e5823-148">Lösen ordet som ska kopplas till tjänstens huvud namn.</span><span class="sxs-lookup"><span data-stu-id="e5823-148">The password to be associated with the service principal.</span></span>

```yaml
Type: SecureString
Parameter Sets: ApplicationWithPasswordPlainParameterSet, DisplayNameWithPasswordPlainParameterSet
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="e5823-149">-PasswordCredentials</span><span class="sxs-lookup"><span data-stu-id="e5823-149">-PasswordCredentials</span></span>
<span data-ttu-id="e5823-150">Listan med autentiseringsuppgifter för lösen ord som är kopplade till tjänstens huvud namn.</span><span class="sxs-lookup"><span data-stu-id="e5823-150">The list of password credentials associated with the service principal.</span></span>

```yaml
Type: PSADPasswordCredential[]
Parameter Sets: ApplicationWithPasswordCredentialParameterSet, DisplayNameWithPasswordCredentialParameterSet
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="e5823-151">-StartDate</span><span class="sxs-lookup"><span data-stu-id="e5823-151">-StartDate</span></span>
<span data-ttu-id="e5823-152">Start datum för användning av autentiseringsuppgifter.</span><span class="sxs-lookup"><span data-stu-id="e5823-152">The effective start date of the credential usage.</span></span>
<span data-ttu-id="e5823-153">Standardvärdet för start datum är idag.</span><span class="sxs-lookup"><span data-stu-id="e5823-153">The default start date value is today.</span></span> <span data-ttu-id="e5823-154">För en "asymmetrisk" typ autentiseringsuppgift måste detta ställas in på eller efter det datum då X509-certifikatet är giltigt från.</span><span class="sxs-lookup"><span data-stu-id="e5823-154">For an "asymmetric" type credential, this must be set to on or after the date that the X509 certificate is valid from.</span></span>

```yaml
Type: DateTime
Parameter Sets: ApplicationWithPasswordPlainParameterSet, ApplicationWithKeyPlainParameterSet, DisplayNameWithPasswordPlainParameterSet, DisplayNameWithKeyPlainParameterSet
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="e5823-155">-Bekräfta</span><span class="sxs-lookup"><span data-stu-id="e5823-155">-Confirm</span></span>
<span data-ttu-id="e5823-156">Du uppmanas att bekräfta innan du kör cmdleten.</span><span class="sxs-lookup"><span data-stu-id="e5823-156">Prompts you for confirmation before running the cmdlet.</span></span>

```yaml
Type: SwitchParameter
Parameter Sets: (All)
Aliases: cf

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="e5823-157">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="e5823-157">-WhatIf</span></span>
```yaml
Type: SwitchParameter
Parameter Sets: (All)
Aliases: wi

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="e5823-158">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="e5823-158">CommonParameters</span></span>
<span data-ttu-id="e5823-159">Den här cmdleten har stöd för de gemensamma parametrarna:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-disvariable,-utbuffer,-PipelineVariable,-verbose,-WarningAction och-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="e5823-159">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="e5823-160">Mer information finns i about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="e5823-160">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="e5823-161">KOSTNADS</span><span class="sxs-lookup"><span data-stu-id="e5823-161">INPUTS</span></span>

### <span data-ttu-id="e5823-162">Ingen</span><span class="sxs-lookup"><span data-stu-id="e5823-162">None</span></span>
<span data-ttu-id="e5823-163">Denna cmdlet accepterar inte indata.</span><span class="sxs-lookup"><span data-stu-id="e5823-163">This cmdlet does not accept any input.</span></span>

## <span data-ttu-id="e5823-164">VÄRDEN</span><span class="sxs-lookup"><span data-stu-id="e5823-164">OUTPUTS</span></span>

### <span data-ttu-id="e5823-165">Microsoft.Azure.Graph.RBAC.Version1_6. ActiveDirectory. PSADServicePrincipal</span><span class="sxs-lookup"><span data-stu-id="e5823-165">Microsoft.Azure.Graph.RBAC.Version1_6.ActiveDirectory.PSADServicePrincipal</span></span>

## <span data-ttu-id="e5823-166">ANMÄRKNINGAR</span><span class="sxs-lookup"><span data-stu-id="e5823-166">NOTES</span></span>
<span data-ttu-id="e5823-167">Nyckelord: Azure, azurerm, arm, resurs, hantering, chef, resurs, grupp, Mall, distribution</span><span class="sxs-lookup"><span data-stu-id="e5823-167">Keywords: azure, azurerm, arm, resource, management, manager, resource, group, template, deployment</span></span>

## <span data-ttu-id="e5823-168">RELATERADE LÄNKAR</span><span class="sxs-lookup"><span data-stu-id="e5823-168">RELATED LINKS</span></span>

[<span data-ttu-id="e5823-169">Remove-AzureRmADServicePrincipal</span><span class="sxs-lookup"><span data-stu-id="e5823-169">Remove-AzureRmADServicePrincipal</span></span>](./Remove-AzureRmADServicePrincipal.md)

[<span data-ttu-id="e5823-170">Get-AzureRmADServicePrincipal</span><span class="sxs-lookup"><span data-stu-id="e5823-170">Get-AzureRmADServicePrincipal</span></span>](./Get-AzureRmADServicePrincipal.md)

[<span data-ttu-id="e5823-171">New-AzureRmADApplication</span><span class="sxs-lookup"><span data-stu-id="e5823-171">New-AzureRmADApplication</span></span>](./New-AzureRmADApplication.md)

[<span data-ttu-id="e5823-172">Remove-AzureRmADApplication</span><span class="sxs-lookup"><span data-stu-id="e5823-172">Remove-AzureRmADApplication</span></span>](./Remove-AzureRmADApplication.md)

[<span data-ttu-id="e5823-173">Get-AzureRmADSpCredential</span><span class="sxs-lookup"><span data-stu-id="e5823-173">Get-AzureRmADSpCredential</span></span>](./Get-AzureRmADSpCredential.md)

[<span data-ttu-id="e5823-174">New-AzureRmADSpCredential</span><span class="sxs-lookup"><span data-stu-id="e5823-174">New-AzureRmADSpCredential</span></span>](./New-AzureRmADSpCredential.md)

[<span data-ttu-id="e5823-175">Remove-AzureRmADSpCredential</span><span class="sxs-lookup"><span data-stu-id="e5823-175">Remove-AzureRmADSpCredential</span></span>](./Remove-AzureRmADSpCredential.md)

