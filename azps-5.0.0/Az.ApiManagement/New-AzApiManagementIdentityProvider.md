---
external help file: Microsoft.Azure.PowerShell.Cmdlets.ApiManagement.ServiceManagement.dll-Help.xml
Module Name: Az.ApiManagement
online version: https://docs.microsoft.com/en-us/powershell/module/az.apimanagement/new-azapimanagementidentityprovider
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/ApiManagement/ApiManagement/help/New-AzApiManagementIdentityProvider.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/ApiManagement/ApiManagement/help/New-AzApiManagementIdentityProvider.md
ms.openlocfilehash: 75f6b7cee1517a3f9ae363a7e28df420e18d37ab
ms.sourcegitcommit: b4a38bcb0501a9016a4998efd377aa75d3ef9ce8
ms.translationtype: MT
ms.contentlocale: sv-SE
ms.lasthandoff: 10/27/2020
ms.locfileid: "94270169"
---
# <span data-ttu-id="04c71-101">New-AzApiManagementIdentityProvider</span><span class="sxs-lookup"><span data-stu-id="04c71-101">New-AzApiManagementIdentityProvider</span></span>

## <span data-ttu-id="04c71-102">Sammanfattning</span><span class="sxs-lookup"><span data-stu-id="04c71-102">SYNOPSIS</span></span>
<span data-ttu-id="04c71-103">Skapar en ny identitets leverantörs konfiguration.</span><span class="sxs-lookup"><span data-stu-id="04c71-103">Creates a new Identity Provider configuration.</span></span>

## <span data-ttu-id="04c71-104">FRÅGESYNTAXEN</span><span class="sxs-lookup"><span data-stu-id="04c71-104">SYNTAX</span></span>

```
New-AzApiManagementIdentityProvider -Context <PsApiManagementContext>
 -Type <PsApiManagementIdentityProviderType> -ClientId <String> -ClientSecret <String>
 [-AllowedTenants <String[]>] [-Authority <String>] [-SignupPolicyName <String>] [-SigninPolicyName <String>]
 [-ProfileEditingPolicyName <String>] [-PasswordResetPolicyName <String>] [-SigninTenant <String>]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="04c71-105">PROBLEMBESKRIVNING</span><span class="sxs-lookup"><span data-stu-id="04c71-105">DESCRIPTION</span></span>
<span data-ttu-id="04c71-106">Skapar en ny identitets leverantörs konfiguration.</span><span class="sxs-lookup"><span data-stu-id="04c71-106">Creates a new Identity Provider configuration.</span></span>

## <span data-ttu-id="04c71-107">BESKRIVS</span><span class="sxs-lookup"><span data-stu-id="04c71-107">EXAMPLES</span></span>

### <span data-ttu-id="04c71-108">Exempel 1: konfigurerar Facebook som identitets leverantör för utvecklare som använder utvecklings portalen</span><span class="sxs-lookup"><span data-stu-id="04c71-108">Example 1: Configures Facebook as an identity Provider for Developer Portal Logins</span></span>
```powershell
PS C:\>$apimContext = New-AzApiManagementContext -ResourceGroupName "Api-Default-WestUS" -ServiceName "contoso"
PS C:\>New-AzApiManagementIdentityProvider -Context $apimContext -Type 'Facebook' -ClientId 'sdfsfwerwerw' -ClientSecret 'sdgsdfgfst43tewfewrf'
```

<span data-ttu-id="04c71-109">Det här kommandot konfigurerar Facebook-identiteten som godkänd identitets leverantör på Developer-portalen för ApiManagement-tjänsten.</span><span class="sxs-lookup"><span data-stu-id="04c71-109">This command configures Facebook Identity as a accepted Identity Provider on the Developer Portal of the ApiManagement service.</span></span>
<span data-ttu-id="04c71-110">Det här kommer att ange ClientId och ClientSecret i Facebook-appen.</span><span class="sxs-lookup"><span data-stu-id="04c71-110">This takes as input the ClientId and ClientSecret of the Facebook app.</span></span>

### <span data-ttu-id="04c71-111">Exempel 2: konfigurerar adB2C som identitets leverantör för utvecklings Portal-inloggningar</span><span class="sxs-lookup"><span data-stu-id="04c71-111">Example 2: Configures adB2C as an identity Provider for Developer Portal Logins</span></span>
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

<span data-ttu-id="04c71-112">Det här kommandot konfigurerar Facebook-identiteten som godkänd identitets leverantör på Developer-portalen för ApiManagement-tjänsten.</span><span class="sxs-lookup"><span data-stu-id="04c71-112">This command configures Facebook Identity as a accepted Identity Provider on the Developer Portal of the ApiManagement service.</span></span>
<span data-ttu-id="04c71-113">Det här kommer att ange ClientId och ClientSecret i Facebook-appen.</span><span class="sxs-lookup"><span data-stu-id="04c71-113">This takes as input the ClientId and ClientSecret of the Facebook app.</span></span>

## <span data-ttu-id="04c71-114">MALLPARAMETRAR</span><span class="sxs-lookup"><span data-stu-id="04c71-114">PARAMETERS</span></span>

### <span data-ttu-id="04c71-115">-AllowedTenants</span><span class="sxs-lookup"><span data-stu-id="04c71-115">-AllowedTenants</span></span>
<span data-ttu-id="04c71-116">Lista över tillåtna Azure Active Directory-klient organisationer</span><span class="sxs-lookup"><span data-stu-id="04c71-116">List of allowed Azure Active Directory Tenants</span></span>

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

### <span data-ttu-id="04c71-117">-Myndighet</span><span class="sxs-lookup"><span data-stu-id="04c71-117">-Authority</span></span>
<span data-ttu-id="04c71-118">Slut punkts namn för OpenID för AAD-eller AAD-B2C.</span><span class="sxs-lookup"><span data-stu-id="04c71-118">OpenID Connect discovery endpoint hostname for AAD or AAD B2C.</span></span> <span data-ttu-id="04c71-119">Denna parameter är valfri.</span><span class="sxs-lookup"><span data-stu-id="04c71-119">This parameter is optional.</span></span>

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

### <span data-ttu-id="04c71-120">-ClientId</span><span class="sxs-lookup"><span data-stu-id="04c71-120">-ClientId</span></span>
<span data-ttu-id="04c71-121">Klient-ID för programmet i extern identitets leverantör.</span><span class="sxs-lookup"><span data-stu-id="04c71-121">Client Id of the Application in the external Identity Provider.</span></span>
<span data-ttu-id="04c71-122">Det är program-ID för Facebook-inloggning, klient-ID för Google-inloggning, app-ID för Microsoft.</span><span class="sxs-lookup"><span data-stu-id="04c71-122">It is App ID for Facebook login, Client ID for Google login, App ID for Microsoft.</span></span>

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

### <span data-ttu-id="04c71-123">-ClientSecret</span><span class="sxs-lookup"><span data-stu-id="04c71-123">-ClientSecret</span></span>
<span data-ttu-id="04c71-124">Klient hemlighet för programmet i extern identitets leverantör som används för att autentisera inloggningsbegäran.</span><span class="sxs-lookup"><span data-stu-id="04c71-124">Client secret of the Application in external Identity Provider, used to authenticate login request.</span></span>
<span data-ttu-id="04c71-125">Det är exempelvis program hemlighet för Facebook-inloggning, API-nyckel för Google-inloggning, offentlig nyckel för Microsoft.</span><span class="sxs-lookup"><span data-stu-id="04c71-125">For example, it is App Secret for Facebook login, API Key for Google login, Public Key for Microsoft.</span></span>

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

### <span data-ttu-id="04c71-126">-Kontext</span><span class="sxs-lookup"><span data-stu-id="04c71-126">-Context</span></span>
<span data-ttu-id="04c71-127">Instans av PsApiManagementContext.</span><span class="sxs-lookup"><span data-stu-id="04c71-127">Instance of PsApiManagementContext.</span></span>
<span data-ttu-id="04c71-128">Denna parameter är obligatorisk.</span><span class="sxs-lookup"><span data-stu-id="04c71-128">This parameter is required.</span></span>

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

### <span data-ttu-id="04c71-129">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="04c71-129">-DefaultProfile</span></span>
<span data-ttu-id="04c71-130">Autentiseringsuppgifter, konto, klient organisation och abonnemang som används för kommunikation med Azure.</span><span class="sxs-lookup"><span data-stu-id="04c71-130">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="04c71-131">-PasswordResetPolicyName</span><span class="sxs-lookup"><span data-stu-id="04c71-131">-PasswordResetPolicyName</span></span>
<span data-ttu-id="04c71-132">Princip namn för återställning av lösen ord.</span><span class="sxs-lookup"><span data-stu-id="04c71-132">Password Reset Policy Name.</span></span> <span data-ttu-id="04c71-133">Gäller endast AAD B2C-identitetsprovider.</span><span class="sxs-lookup"><span data-stu-id="04c71-133">Only applies to AAD B2C Identity Provider.</span></span> <span data-ttu-id="04c71-134">Denna parameter är valfri.</span><span class="sxs-lookup"><span data-stu-id="04c71-134">This parameter is optional.</span></span>

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

### <span data-ttu-id="04c71-135">-ProfileEditingPolicyName</span><span class="sxs-lookup"><span data-stu-id="04c71-135">-ProfileEditingPolicyName</span></span>
<span data-ttu-id="04c71-136">Princip namn för profil redigering.</span><span class="sxs-lookup"><span data-stu-id="04c71-136">Profile Editing Policy Name.</span></span> <span data-ttu-id="04c71-137">Gäller endast AAD B2C-identitetsprovider.</span><span class="sxs-lookup"><span data-stu-id="04c71-137">Only applies to AAD B2C Identity Provider.</span></span> <span data-ttu-id="04c71-138">Denna parameter är valfri.</span><span class="sxs-lookup"><span data-stu-id="04c71-138">This parameter is optional.</span></span>

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

### <span data-ttu-id="04c71-139">-SigninPolicyName</span><span class="sxs-lookup"><span data-stu-id="04c71-139">-SigninPolicyName</span></span>
<span data-ttu-id="04c71-140">Inloggnings princip namn.</span><span class="sxs-lookup"><span data-stu-id="04c71-140">Signin Policy Name.</span></span> <span data-ttu-id="04c71-141">Gäller endast AAD B2C-identitetsprovider.</span><span class="sxs-lookup"><span data-stu-id="04c71-141">Only applies to AAD B2C Identity Provider.</span></span> <span data-ttu-id="04c71-142">Denna parameter är valfri.</span><span class="sxs-lookup"><span data-stu-id="04c71-142">This parameter is optional.</span></span>

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

### <span data-ttu-id="04c71-143">-SigninTenant</span><span class="sxs-lookup"><span data-stu-id="04c71-143">-SigninTenant</span></span>
<span data-ttu-id="04c71-144">Logga in klient organisationen för att åsidosätta i AAD B2C i stället för `common` klient organisationen</span><span class="sxs-lookup"><span data-stu-id="04c71-144">Signin Tenant to override in AAD B2C instead of the `common` Tenant</span></span>

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

### <span data-ttu-id="04c71-145">-SignupPolicyName</span><span class="sxs-lookup"><span data-stu-id="04c71-145">-SignupPolicyName</span></span>
<span data-ttu-id="04c71-146">Namn på registrerings policy.</span><span class="sxs-lookup"><span data-stu-id="04c71-146">Signup Policy Name.</span></span> <span data-ttu-id="04c71-147">Gäller endast AAD B2C-identitetsprovider.</span><span class="sxs-lookup"><span data-stu-id="04c71-147">Only applies to AAD B2C Identity Provider.</span></span> <span data-ttu-id="04c71-148">Denna parameter är valfri.</span><span class="sxs-lookup"><span data-stu-id="04c71-148">This parameter is optional.</span></span>

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

### <span data-ttu-id="04c71-149">– Skriv</span><span class="sxs-lookup"><span data-stu-id="04c71-149">-Type</span></span>
<span data-ttu-id="04c71-150">Identifierare för en identitets leverantör.</span><span class="sxs-lookup"><span data-stu-id="04c71-150">Identifier of a Identity Provider.</span></span>
<span data-ttu-id="04c71-151">Om det här alternativet anges kan du hitta identitets leverantörens konfiguration enligt ID.</span><span class="sxs-lookup"><span data-stu-id="04c71-151">If specified will try to find identity provider configuration by the identifier.</span></span>
<span data-ttu-id="04c71-152">Denna parameter är valfri.</span><span class="sxs-lookup"><span data-stu-id="04c71-152">This parameter is optional.</span></span>

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

### <span data-ttu-id="04c71-153">-Bekräfta</span><span class="sxs-lookup"><span data-stu-id="04c71-153">-Confirm</span></span>
<span data-ttu-id="04c71-154">Du uppmanas att bekräfta innan du kör cmdleten.</span><span class="sxs-lookup"><span data-stu-id="04c71-154">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="04c71-155">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="04c71-155">-WhatIf</span></span>
<span data-ttu-id="04c71-156">Visar vad som händer om cmdleten körs.</span><span class="sxs-lookup"><span data-stu-id="04c71-156">Shows what would happen if the cmdlet runs.</span></span> <span data-ttu-id="04c71-157">Cmdleten körs inte.</span><span class="sxs-lookup"><span data-stu-id="04c71-157">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="04c71-158">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="04c71-158">CommonParameters</span></span>
<span data-ttu-id="04c71-159">Den här cmdleten har stöd för de gemensamma parametrarna:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-disvariable,-utbuffer,-PipelineVariable,-verbose,-WarningAction och-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="04c71-159">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="04c71-160">Mer information finns i [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="04c71-160">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="04c71-161">KOSTNADS</span><span class="sxs-lookup"><span data-stu-id="04c71-161">INPUTS</span></span>

### <span data-ttu-id="04c71-162">Microsoft. Azure. commands. ApiManagement. ServiceManagement. Models. PsApiManagementContext</span><span class="sxs-lookup"><span data-stu-id="04c71-162">Microsoft.Azure.Commands.ApiManagement.ServiceManagement.Models.PsApiManagementContext</span></span>

### <span data-ttu-id="04c71-163">Microsoft. Azure. commands. ApiManagement. ServiceManagement. Models. PsApiManagementIdentityProviderType</span><span class="sxs-lookup"><span data-stu-id="04c71-163">Microsoft.Azure.Commands.ApiManagement.ServiceManagement.Models.PsApiManagementIdentityProviderType</span></span>

### <span data-ttu-id="04c71-164">System. String</span><span class="sxs-lookup"><span data-stu-id="04c71-164">System.String</span></span>

### <span data-ttu-id="04c71-165">System. string []</span><span class="sxs-lookup"><span data-stu-id="04c71-165">System.String[]</span></span>

## <span data-ttu-id="04c71-166">VÄRDEN</span><span class="sxs-lookup"><span data-stu-id="04c71-166">OUTPUTS</span></span>

### <span data-ttu-id="04c71-167">Microsoft. Azure. commands. ApiManagement. ServiceManagement. Models. PsApiManagementIdentityProvider</span><span class="sxs-lookup"><span data-stu-id="04c71-167">Microsoft.Azure.Commands.ApiManagement.ServiceManagement.Models.PsApiManagementIdentityProvider</span></span>

## <span data-ttu-id="04c71-168">ANMÄRKNINGAR</span><span class="sxs-lookup"><span data-stu-id="04c71-168">NOTES</span></span>

## <span data-ttu-id="04c71-169">RELATERADE LÄNKAR</span><span class="sxs-lookup"><span data-stu-id="04c71-169">RELATED LINKS</span></span>

[<span data-ttu-id="04c71-170">Get-AzApiManagementIdentityProvider</span><span class="sxs-lookup"><span data-stu-id="04c71-170">Get-AzApiManagementIdentityProvider</span></span>](./Get-AzApiManagementIdentityProvider.md)

[<span data-ttu-id="04c71-171">Remove-AzApiManagementIdentityProvider</span><span class="sxs-lookup"><span data-stu-id="04c71-171">Remove-AzApiManagementIdentityProvider</span></span>](./Remove-AzApiManagementIdentityProvider.md)

[<span data-ttu-id="04c71-172">Set-AzApiManagementIdentityProvider</span><span class="sxs-lookup"><span data-stu-id="04c71-172">Set-AzApiManagementIdentityProvider</span></span>](./Set-AzApiManagementIdentityProvider.md)
