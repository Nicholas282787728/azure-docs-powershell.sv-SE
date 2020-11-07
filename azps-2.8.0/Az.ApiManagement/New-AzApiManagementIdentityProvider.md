---
external help file: Microsoft.Azure.PowerShell.Cmdlets.ApiManagement.ServiceManagement.dll-Help.xml
Module Name: Az.ApiManagement
online version: https://docs.microsoft.com/en-us/powershell/module/az.apimanagement/new-azapimanagementidentityprovider
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/ApiManagement/ApiManagement/help/New-AzApiManagementIdentityProvider.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/ApiManagement/ApiManagement/help/New-AzApiManagementIdentityProvider.md
ms.openlocfilehash: fc033eb1989838d8ed8e20d568f92ef20f8275e8
ms.sourcegitcommit: 4d2c178cd6df9151877b08d54c1f4a228dbec9d1
ms.translationtype: MT
ms.contentlocale: sv-SE
ms.lasthandoff: 01/29/2020
ms.locfileid: "93745767"
---
# <span data-ttu-id="f10ca-101">New-AzApiManagementIdentityProvider</span><span class="sxs-lookup"><span data-stu-id="f10ca-101">New-AzApiManagementIdentityProvider</span></span>

## <span data-ttu-id="f10ca-102">Sammanfattning</span><span class="sxs-lookup"><span data-stu-id="f10ca-102">SYNOPSIS</span></span>
<span data-ttu-id="f10ca-103">Skapar en ny identitets leverantörs konfiguration.</span><span class="sxs-lookup"><span data-stu-id="f10ca-103">Creates a new Identity Provider configuration.</span></span>

## <span data-ttu-id="f10ca-104">FRÅGESYNTAXEN</span><span class="sxs-lookup"><span data-stu-id="f10ca-104">SYNTAX</span></span>

```
New-AzApiManagementIdentityProvider -Context <PsApiManagementContext>
 -Type <PsApiManagementIdentityProviderType> -ClientId <String> -ClientSecret <String>
 [-AllowedTenants <String[]>] [-Authority <String>] [-SignupPolicyName <String>] [-SigninPolicyName <String>]
 [-ProfileEditingPolicyName <String>] [-PasswordResetPolicyName <String>]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="f10ca-105">PROBLEMBESKRIVNING</span><span class="sxs-lookup"><span data-stu-id="f10ca-105">DESCRIPTION</span></span>
<span data-ttu-id="f10ca-106">Skapar en ny identitets leverantörs konfiguration.</span><span class="sxs-lookup"><span data-stu-id="f10ca-106">Creates a new Identity Provider configuration.</span></span>

## <span data-ttu-id="f10ca-107">BESKRIVS</span><span class="sxs-lookup"><span data-stu-id="f10ca-107">EXAMPLES</span></span>

### <span data-ttu-id="f10ca-108">Exempel 1: konfigurerar Facebook som identitets leverantör för utvecklare som använder utvecklings portalen</span><span class="sxs-lookup"><span data-stu-id="f10ca-108">Example 1: Configures Facebook as an identity Provider for Developer Portal Logins</span></span>
```powershell
PS C:\>$apimContext = New-AzApiManagementContext -ResourceGroupName "Api-Default-WestUS" -ServiceName "contoso"
PS C:\>New-AzApiManagementIdentityProvider -Context $apimContext -Type 'Facebook' -ClientId 'sdfsfwerwerw' -ClientSecret 'sdgsdfgfst43tewfewrf'
```

<span data-ttu-id="f10ca-109">Det här kommandot konfigurerar Facebook-identiteten som godkänd identitets leverantör på Developer-portalen för ApiManagement-tjänsten.</span><span class="sxs-lookup"><span data-stu-id="f10ca-109">This command configures Facebook Identity as a accepted Identity Provider on the Developer Portal of the ApiManagement service.</span></span>
<span data-ttu-id="f10ca-110">Det här kommer att ange ClientId och ClientSecret i Facebook-appen.</span><span class="sxs-lookup"><span data-stu-id="f10ca-110">This takes as input the ClientId and ClientSecret of the Facebook app.</span></span>

### <span data-ttu-id="f10ca-111">Exempel 2: konfigurerar adB2C som identitets leverantör för utvecklings Portal-inloggningar</span><span class="sxs-lookup"><span data-stu-id="f10ca-111">Example 2: Configures adB2C as an identity Provider for Developer Portal Logins</span></span>
```powershell
PS C:\>$apimContext = New-AzApiManagementContext -ResourceGroupName "Api-Default-WestUS" -ServiceName "contoso"
PS C:\>New-AzApiManagementIdentityProvider -Context $context -Type AadB2C -ClientId 6b1fc750-9e68-450c-97d2-ba6acd0fbc20 -ClientSecret "foobar" -AllowedTenants 'samirtestbc.onmicrosoft.com' -SignupPolicyName B2C_1_signup-policy

Type                     : AadB2C
ClientId                 : 6b1fc750-9e68-450c-97d2-ba6acd0fbc20
ClientSecret             : foobar
AllowedTenants           : {samirtestbc.onmicrosoft.com}
Authority                : login.microsoftonline.com
SignupPolicyName         : B2C_1_signup-policy
SigninPolicyName         :
ProfileEditingPolicyName :
PasswordResetPolicyName  :
Id                       : /subscriptions/subid/resourceGroups/Api-Default-WestUS/providers/Microsoft.ApiManagement/service/contoso/identityProviders/AadB2C
ResourceGroupName        : Api-Default-WestUS
ServiceName              : contoso
```

<span data-ttu-id="f10ca-112">Det här kommandot konfigurerar Facebook-identiteten som godkänd identitets leverantör på Developer-portalen för ApiManagement-tjänsten.</span><span class="sxs-lookup"><span data-stu-id="f10ca-112">This command configures Facebook Identity as a accepted Identity Provider on the Developer Portal of the ApiManagement service.</span></span>
<span data-ttu-id="f10ca-113">Det här kommer att ange ClientId och ClientSecret i Facebook-appen.</span><span class="sxs-lookup"><span data-stu-id="f10ca-113">This takes as input the ClientId and ClientSecret of the Facebook app.</span></span>

## <span data-ttu-id="f10ca-114">MALLPARAMETRAR</span><span class="sxs-lookup"><span data-stu-id="f10ca-114">PARAMETERS</span></span>

### <span data-ttu-id="f10ca-115">-AllowedTenants</span><span class="sxs-lookup"><span data-stu-id="f10ca-115">-AllowedTenants</span></span>
<span data-ttu-id="f10ca-116">Lista över tillåtna Azure Active Directory-klient organisationer</span><span class="sxs-lookup"><span data-stu-id="f10ca-116">List of allowed Azure Active Directory Tenants</span></span>

```yaml
Type: System.String[]
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="f10ca-117">-Myndighet</span><span class="sxs-lookup"><span data-stu-id="f10ca-117">-Authority</span></span>
<span data-ttu-id="f10ca-118">Slut punkts namn för OpenID för AAD-eller AAD-B2C.</span><span class="sxs-lookup"><span data-stu-id="f10ca-118">OpenID Connect discovery endpoint hostname for AAD or AAD B2C.</span></span> <span data-ttu-id="f10ca-119">Denna parameter är valfri.</span><span class="sxs-lookup"><span data-stu-id="f10ca-119">This parameter is optional.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="f10ca-120">-ClientId</span><span class="sxs-lookup"><span data-stu-id="f10ca-120">-ClientId</span></span>
<span data-ttu-id="f10ca-121">Klient-ID för programmet i extern identitets leverantör.</span><span class="sxs-lookup"><span data-stu-id="f10ca-121">Client Id of the Application in the external Identity Provider.</span></span>
<span data-ttu-id="f10ca-122">Det är program-ID för Facebook-inloggning, klient-ID för Google-inloggning, app-ID för Microsoft.</span><span class="sxs-lookup"><span data-stu-id="f10ca-122">It is App ID for Facebook login, Client ID for Google login, App ID for Microsoft.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="f10ca-123">-ClientSecret</span><span class="sxs-lookup"><span data-stu-id="f10ca-123">-ClientSecret</span></span>
<span data-ttu-id="f10ca-124">Klient hemlighet för programmet i extern identitets leverantör som används för att autentisera inloggningsbegäran.</span><span class="sxs-lookup"><span data-stu-id="f10ca-124">Client secret of the Application in external Identity Provider, used to authenticate login request.</span></span>
<span data-ttu-id="f10ca-125">Det är exempelvis program hemlighet för Facebook-inloggning, API-nyckel för Google-inloggning, offentlig nyckel för Microsoft.</span><span class="sxs-lookup"><span data-stu-id="f10ca-125">For example, it is App Secret for Facebook login, API Key for Google login, Public Key for Microsoft.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="f10ca-126">-Kontext</span><span class="sxs-lookup"><span data-stu-id="f10ca-126">-Context</span></span>
<span data-ttu-id="f10ca-127">Instans av PsApiManagementContext.</span><span class="sxs-lookup"><span data-stu-id="f10ca-127">Instance of PsApiManagementContext.</span></span>
<span data-ttu-id="f10ca-128">Denna parameter är obligatorisk.</span><span class="sxs-lookup"><span data-stu-id="f10ca-128">This parameter is required.</span></span>

```yaml
Type: Microsoft.Azure.Commands.ApiManagement.ServiceManagement.Models.PsApiManagementContext
Parameter Sets: (All)
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName, ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="f10ca-129">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="f10ca-129">-DefaultProfile</span></span>
<span data-ttu-id="f10ca-130">Autentiseringsuppgifter, konto, klient organisation och abonnemang som används för kommunikation med Azure.</span><span class="sxs-lookup"><span data-stu-id="f10ca-130">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="f10ca-131">-PasswordResetPolicyName</span><span class="sxs-lookup"><span data-stu-id="f10ca-131">-PasswordResetPolicyName</span></span>
<span data-ttu-id="f10ca-132">Princip namn för återställning av lösen ord.</span><span class="sxs-lookup"><span data-stu-id="f10ca-132">Password Reset Policy Name.</span></span> <span data-ttu-id="f10ca-133">Gäller endast AAD B2C-identitetsprovider.</span><span class="sxs-lookup"><span data-stu-id="f10ca-133">Only applies to AAD B2C Identity Provider.</span></span> <span data-ttu-id="f10ca-134">Denna parameter är valfri.</span><span class="sxs-lookup"><span data-stu-id="f10ca-134">This parameter is optional.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="f10ca-135">-ProfileEditingPolicyName</span><span class="sxs-lookup"><span data-stu-id="f10ca-135">-ProfileEditingPolicyName</span></span>
<span data-ttu-id="f10ca-136">Princip namn för profil redigering.</span><span class="sxs-lookup"><span data-stu-id="f10ca-136">Profile Editing Policy Name.</span></span> <span data-ttu-id="f10ca-137">Gäller endast AAD B2C-identitetsprovider.</span><span class="sxs-lookup"><span data-stu-id="f10ca-137">Only applies to AAD B2C Identity Provider.</span></span> <span data-ttu-id="f10ca-138">Denna parameter är valfri.</span><span class="sxs-lookup"><span data-stu-id="f10ca-138">This parameter is optional.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="f10ca-139">-SigninPolicyName</span><span class="sxs-lookup"><span data-stu-id="f10ca-139">-SigninPolicyName</span></span>
<span data-ttu-id="f10ca-140">Inloggnings princip namn.</span><span class="sxs-lookup"><span data-stu-id="f10ca-140">Signin Policy Name.</span></span> <span data-ttu-id="f10ca-141">Gäller endast AAD B2C-identitetsprovider.</span><span class="sxs-lookup"><span data-stu-id="f10ca-141">Only applies to AAD B2C Identity Provider.</span></span> <span data-ttu-id="f10ca-142">Denna parameter är valfri.</span><span class="sxs-lookup"><span data-stu-id="f10ca-142">This parameter is optional.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="f10ca-143">-SignupPolicyName</span><span class="sxs-lookup"><span data-stu-id="f10ca-143">-SignupPolicyName</span></span>
<span data-ttu-id="f10ca-144">Namn på registrerings policy.</span><span class="sxs-lookup"><span data-stu-id="f10ca-144">Signup Policy Name.</span></span> <span data-ttu-id="f10ca-145">Gäller endast AAD B2C-identitetsprovider.</span><span class="sxs-lookup"><span data-stu-id="f10ca-145">Only applies to AAD B2C Identity Provider.</span></span> <span data-ttu-id="f10ca-146">Denna parameter är valfri.</span><span class="sxs-lookup"><span data-stu-id="f10ca-146">This parameter is optional.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="f10ca-147">– Skriv</span><span class="sxs-lookup"><span data-stu-id="f10ca-147">-Type</span></span>
<span data-ttu-id="f10ca-148">Identifierare för en identitets leverantör.</span><span class="sxs-lookup"><span data-stu-id="f10ca-148">Identifier of a Identity Provider.</span></span>
<span data-ttu-id="f10ca-149">Om det här alternativet anges kan du hitta identitets leverantörens konfiguration enligt ID.</span><span class="sxs-lookup"><span data-stu-id="f10ca-149">If specified will try to find identity provider configuration by the identifier.</span></span>
<span data-ttu-id="f10ca-150">Denna parameter är valfri.</span><span class="sxs-lookup"><span data-stu-id="f10ca-150">This parameter is optional.</span></span>

```yaml
Type: Microsoft.Azure.Commands.ApiManagement.ServiceManagement.Models.PsApiManagementIdentityProviderType
Parameter Sets: (All)
Aliases:
Accepted values: Facebook, Google, Microsoft, Twitter, Aad, AadB2C

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="f10ca-151">-Bekräfta</span><span class="sxs-lookup"><span data-stu-id="f10ca-151">-Confirm</span></span>
<span data-ttu-id="f10ca-152">Du uppmanas att bekräfta innan du kör cmdleten.</span><span class="sxs-lookup"><span data-stu-id="f10ca-152">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="f10ca-153">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="f10ca-153">-WhatIf</span></span>
<span data-ttu-id="f10ca-154">Visar vad som händer om cmdleten körs.</span><span class="sxs-lookup"><span data-stu-id="f10ca-154">Shows what would happen if the cmdlet runs.</span></span> <span data-ttu-id="f10ca-155">Cmdleten körs inte.</span><span class="sxs-lookup"><span data-stu-id="f10ca-155">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="f10ca-156">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="f10ca-156">CommonParameters</span></span>
<span data-ttu-id="f10ca-157">Den här cmdleten har stöd för de gemensamma parametrarna:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-disvariable,-utbuffer,-PipelineVariable,-verbose,-WarningAction och-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="f10ca-157">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="f10ca-158">Mer information finns i [about_CommonParameters](https://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="f10ca-158">For more information, see [about_CommonParameters](https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="f10ca-159">KOSTNADS</span><span class="sxs-lookup"><span data-stu-id="f10ca-159">INPUTS</span></span>

### <span data-ttu-id="f10ca-160">Microsoft. Azure. commands. ApiManagement. ServiceManagement. Models. PsApiManagementContext</span><span class="sxs-lookup"><span data-stu-id="f10ca-160">Microsoft.Azure.Commands.ApiManagement.ServiceManagement.Models.PsApiManagementContext</span></span>

### <span data-ttu-id="f10ca-161">Microsoft. Azure. commands. ApiManagement. ServiceManagement. Models. PsApiManagementIdentityProviderType</span><span class="sxs-lookup"><span data-stu-id="f10ca-161">Microsoft.Azure.Commands.ApiManagement.ServiceManagement.Models.PsApiManagementIdentityProviderType</span></span>

### <span data-ttu-id="f10ca-162">System. String</span><span class="sxs-lookup"><span data-stu-id="f10ca-162">System.String</span></span>

### <span data-ttu-id="f10ca-163">System. string []</span><span class="sxs-lookup"><span data-stu-id="f10ca-163">System.String[]</span></span>

## <span data-ttu-id="f10ca-164">VÄRDEN</span><span class="sxs-lookup"><span data-stu-id="f10ca-164">OUTPUTS</span></span>

### <span data-ttu-id="f10ca-165">Microsoft. Azure. commands. ApiManagement. ServiceManagement. Models. PsApiManagementIdentityProvider</span><span class="sxs-lookup"><span data-stu-id="f10ca-165">Microsoft.Azure.Commands.ApiManagement.ServiceManagement.Models.PsApiManagementIdentityProvider</span></span>

## <span data-ttu-id="f10ca-166">ANMÄRKNINGAR</span><span class="sxs-lookup"><span data-stu-id="f10ca-166">NOTES</span></span>

## <span data-ttu-id="f10ca-167">RELATERADE LÄNKAR</span><span class="sxs-lookup"><span data-stu-id="f10ca-167">RELATED LINKS</span></span>

[<span data-ttu-id="f10ca-168">Get-AzApiManagementIdentityProvider</span><span class="sxs-lookup"><span data-stu-id="f10ca-168">Get-AzApiManagementIdentityProvider</span></span>](./Get-AzApiManagementIdentityProvider.md)

[<span data-ttu-id="f10ca-169">Remove-AzApiManagementIdentityProvider</span><span class="sxs-lookup"><span data-stu-id="f10ca-169">Remove-AzApiManagementIdentityProvider</span></span>](./Remove-AzApiManagementIdentityProvider.md)

[<span data-ttu-id="f10ca-170">Set-AzApiManagementIdentityProvider</span><span class="sxs-lookup"><span data-stu-id="f10ca-170">Set-AzApiManagementIdentityProvider</span></span>](./Set-AzApiManagementIdentityProvider.md)
