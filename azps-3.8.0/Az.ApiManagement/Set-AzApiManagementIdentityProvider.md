---
external help file: Microsoft.Azure.PowerShell.Cmdlets.ApiManagement.ServiceManagement.dll-Help.xml
Module Name: Az.ApiManagement
online version: https://docs.microsoft.com/en-us/powershell/module/az.apimanagement/set-azapimanagementidentityprovider
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/ApiManagement/ApiManagement/help/Set-AzApiManagementIdentityProvider.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/ApiManagement/ApiManagement/help/Set-AzApiManagementIdentityProvider.md
ms.openlocfilehash: a110e950bff46bba7d3c7b5033c01b95ac2397f1
ms.sourcegitcommit: 6a91b4c545350d316d3cf8c62f384478e3f3ba24
ms.translationtype: MT
ms.contentlocale: sv-SE
ms.lasthandoff: 04/21/2020
ms.locfileid: "94091581"
---
# <span data-ttu-id="d9bbb-101">Set-AzApiManagementIdentityProvider</span><span class="sxs-lookup"><span data-stu-id="d9bbb-101">Set-AzApiManagementIdentityProvider</span></span>

## <span data-ttu-id="d9bbb-102">Sammanfattning</span><span class="sxs-lookup"><span data-stu-id="d9bbb-102">SYNOPSIS</span></span>
<span data-ttu-id="d9bbb-103">Uppdaterar konfigurationen för en befintlig identitets leverantör.</span><span class="sxs-lookup"><span data-stu-id="d9bbb-103">Updates the Configuration of an existing Identity Provider.</span></span>

## <span data-ttu-id="d9bbb-104">FRÅGESYNTAXEN</span><span class="sxs-lookup"><span data-stu-id="d9bbb-104">SYNTAX</span></span>

### <span data-ttu-id="d9bbb-105">ExpandedParameter (standard)</span><span class="sxs-lookup"><span data-stu-id="d9bbb-105">ExpandedParameter (Default)</span></span>
```
Set-AzApiManagementIdentityProvider -Context <PsApiManagementContext>
 -Type <PsApiManagementIdentityProviderType> [-ClientId <String>] [-ClientSecret <String>]
 [-AllowedTenants <String[]>] [-Authority <String>] [-SignupPolicyName <String>] [-SigninPolicyName <String>]
 [-ProfileEditingPolicyName <String>] [-PasswordResetPolicyName <String>] [-SignInTenant <String>] [-PassThru]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="d9bbb-106">ByInputObject</span><span class="sxs-lookup"><span data-stu-id="d9bbb-106">ByInputObject</span></span>
```
Set-AzApiManagementIdentityProvider -InputObject <PsApiManagementIdentityProvider> [-ClientId <String>]
 [-ClientSecret <String>] [-AllowedTenants <String[]>] [-Authority <String>] [-SignupPolicyName <String>]
 [-SigninPolicyName <String>] [-ProfileEditingPolicyName <String>] [-PasswordResetPolicyName <String>]
 [-SignInTenant <String>] [-PassThru] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="d9bbb-107">PROBLEMBESKRIVNING</span><span class="sxs-lookup"><span data-stu-id="d9bbb-107">DESCRIPTION</span></span>
<span data-ttu-id="d9bbb-108">Uppdaterar konfigurationen för en befintlig identitets leverantör.</span><span class="sxs-lookup"><span data-stu-id="d9bbb-108">Updates the Configuration of an existing Identity Provider.</span></span>

## <span data-ttu-id="d9bbb-109">BESKRIVS</span><span class="sxs-lookup"><span data-stu-id="d9bbb-109">EXAMPLES</span></span>

### <span data-ttu-id="d9bbb-110">Exempel 1: uppdatera Facebook-identitetsprovider</span><span class="sxs-lookup"><span data-stu-id="d9bbb-110">Example 1 : Update the facebook Identity Provider</span></span>
```powershell
PS C:\>$apimContext = New-AzApiManagementContext -ResourceGroupName "Api-Default-WestUS" -ServiceName "contoso"
PS C:\> Set-AzApiManagementIdentityProvider -Context $apimContext -Type Facebook -ClientSecret "updatedSecret" -PassThru
```

<span data-ttu-id="d9bbb-111">Cmdleten uppdaterar Facebook-identitets leverantörens klient hemlighet;</span><span class="sxs-lookup"><span data-stu-id="d9bbb-111">The cmdlet updates the Client Secret of the Facebook Identity Provider;</span></span>

## <span data-ttu-id="d9bbb-112">MALLPARAMETRAR</span><span class="sxs-lookup"><span data-stu-id="d9bbb-112">PARAMETERS</span></span>

### <span data-ttu-id="d9bbb-113">-AllowedTenants</span><span class="sxs-lookup"><span data-stu-id="d9bbb-113">-AllowedTenants</span></span>
<span data-ttu-id="d9bbb-114">Lista över tillåtna Azure Active Directory-klient organisationer.</span><span class="sxs-lookup"><span data-stu-id="d9bbb-114">List of allowed Azure Active Directory Tenants.</span></span>

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

### <span data-ttu-id="d9bbb-115">-Myndighet</span><span class="sxs-lookup"><span data-stu-id="d9bbb-115">-Authority</span></span>
<span data-ttu-id="d9bbb-116">Slut punkts namn för OpenID för AAD-eller AAD-B2C.</span><span class="sxs-lookup"><span data-stu-id="d9bbb-116">OpenID Connect discovery endpoint hostname for AAD or AAD B2C.</span></span> <span data-ttu-id="d9bbb-117">Denna parameter är valfri.</span><span class="sxs-lookup"><span data-stu-id="d9bbb-117">This parameter is optional.</span></span>

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

### <span data-ttu-id="d9bbb-118">-ClientId</span><span class="sxs-lookup"><span data-stu-id="d9bbb-118">-ClientId</span></span>
<span data-ttu-id="d9bbb-119">Klient-ID för programmet i extern identitets leverantör.</span><span class="sxs-lookup"><span data-stu-id="d9bbb-119">Client Id of the Application in the external Identity Provider.</span></span>
<span data-ttu-id="d9bbb-120">Det är program-ID för Facebook-inloggning, klient-ID för Google-inloggning, app-ID för Microsoft.</span><span class="sxs-lookup"><span data-stu-id="d9bbb-120">It is App ID for Facebook login, Client ID for Google login, App ID for Microsoft.</span></span>

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

### <span data-ttu-id="d9bbb-121">-ClientSecret</span><span class="sxs-lookup"><span data-stu-id="d9bbb-121">-ClientSecret</span></span>
<span data-ttu-id="d9bbb-122">Klient hemlighet för programmet i extern identitets leverantör som används för att autentisera inloggningsbegäran.</span><span class="sxs-lookup"><span data-stu-id="d9bbb-122">Client secret of the Application in external Identity Provider, used to authenticate login request.</span></span>
<span data-ttu-id="d9bbb-123">Det är exempelvis program hemlighet för Facebook-inloggning, API-nyckel för Google-inloggning, offentlig nyckel för Microsoft.</span><span class="sxs-lookup"><span data-stu-id="d9bbb-123">For example, it is App Secret for Facebook login, API Key for Google login, Public Key for Microsoft.</span></span>

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

### <span data-ttu-id="d9bbb-124">-Kontext</span><span class="sxs-lookup"><span data-stu-id="d9bbb-124">-Context</span></span>
<span data-ttu-id="d9bbb-125">Instans av PsApiManagementContext.</span><span class="sxs-lookup"><span data-stu-id="d9bbb-125">Instance of PsApiManagementContext.</span></span>
<span data-ttu-id="d9bbb-126">Denna parameter är obligatorisk.</span><span class="sxs-lookup"><span data-stu-id="d9bbb-126">This parameter is required.</span></span>

```yaml
Type: Microsoft.Azure.Commands.ApiManagement.ServiceManagement.Models.PsApiManagementContext
Parameter Sets: ExpandedParameter
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName, ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="d9bbb-127">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="d9bbb-127">-DefaultProfile</span></span>
<span data-ttu-id="d9bbb-128">Autentiseringsuppgifter, konto, klient organisation och abonnemang som används för kommunikation med Azure.</span><span class="sxs-lookup"><span data-stu-id="d9bbb-128">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="d9bbb-129">-InputObject</span><span class="sxs-lookup"><span data-stu-id="d9bbb-129">-InputObject</span></span>
<span data-ttu-id="d9bbb-130">Instans av PsApiManagementIdentityProvider.</span><span class="sxs-lookup"><span data-stu-id="d9bbb-130">Instance of PsApiManagementIdentityProvider.</span></span> <span data-ttu-id="d9bbb-131">Denna parameter är obligatorisk.</span><span class="sxs-lookup"><span data-stu-id="d9bbb-131">This parameter is required.</span></span>

```yaml
Type: Microsoft.Azure.Commands.ApiManagement.ServiceManagement.Models.PsApiManagementIdentityProvider
Parameter Sets: ByInputObject
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="d9bbb-132">-PassThru</span><span class="sxs-lookup"><span data-stu-id="d9bbb-132">-PassThru</span></span>
<span data-ttu-id="d9bbb-133">Anger att denna cmdlet returnerar  **PsApiManagementIdentityProvider** som denna cmdlet ändrar.</span><span class="sxs-lookup"><span data-stu-id="d9bbb-133">Indicates that this cmdlet returns the  **PsApiManagementIdentityProvider** that this cmdlet modifies.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="d9bbb-134">-PasswordResetPolicyName</span><span class="sxs-lookup"><span data-stu-id="d9bbb-134">-PasswordResetPolicyName</span></span>
<span data-ttu-id="d9bbb-135">Princip namn för återställning av lösen ord.</span><span class="sxs-lookup"><span data-stu-id="d9bbb-135">Password Reset Policy Name.</span></span> <span data-ttu-id="d9bbb-136">Gäller endast AAD B2C-identitetsprovider.</span><span class="sxs-lookup"><span data-stu-id="d9bbb-136">Only applies to AAD B2C Identity Provider.</span></span> <span data-ttu-id="d9bbb-137">Denna parameter är valfri.</span><span class="sxs-lookup"><span data-stu-id="d9bbb-137">This parameter is optional.</span></span>

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

### <span data-ttu-id="d9bbb-138">-ProfileEditingPolicyName</span><span class="sxs-lookup"><span data-stu-id="d9bbb-138">-ProfileEditingPolicyName</span></span>
<span data-ttu-id="d9bbb-139">Princip namn för profil redigering.</span><span class="sxs-lookup"><span data-stu-id="d9bbb-139">Profile Editing Policy Name.</span></span> <span data-ttu-id="d9bbb-140">Gäller endast AAD B2C-identitetsprovider.</span><span class="sxs-lookup"><span data-stu-id="d9bbb-140">Only applies to AAD B2C Identity Provider.</span></span> <span data-ttu-id="d9bbb-141">Denna parameter är valfri.</span><span class="sxs-lookup"><span data-stu-id="d9bbb-141">This parameter is optional.</span></span>

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

### <span data-ttu-id="d9bbb-142">-SigninPolicyName</span><span class="sxs-lookup"><span data-stu-id="d9bbb-142">-SigninPolicyName</span></span>
<span data-ttu-id="d9bbb-143">Inloggnings princip namn.</span><span class="sxs-lookup"><span data-stu-id="d9bbb-143">Signin Policy Name.</span></span> <span data-ttu-id="d9bbb-144">Gäller endast AAD B2C-identitetsprovider.</span><span class="sxs-lookup"><span data-stu-id="d9bbb-144">Only applies to AAD B2C Identity Provider.</span></span> <span data-ttu-id="d9bbb-145">Denna parameter är valfri.</span><span class="sxs-lookup"><span data-stu-id="d9bbb-145">This parameter is optional.</span></span>

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

### <span data-ttu-id="d9bbb-146">-SignupPolicyName</span><span class="sxs-lookup"><span data-stu-id="d9bbb-146">-SignupPolicyName</span></span>
<span data-ttu-id="d9bbb-147">Namn på registrerings policy.</span><span class="sxs-lookup"><span data-stu-id="d9bbb-147">Signup Policy Name.</span></span> <span data-ttu-id="d9bbb-148">Gäller endast AAD B2C-identitetsprovider.</span><span class="sxs-lookup"><span data-stu-id="d9bbb-148">Only applies to AAD B2C Identity Provider.</span></span> <span data-ttu-id="d9bbb-149">Denna parameter är valfri.</span><span class="sxs-lookup"><span data-stu-id="d9bbb-149">This parameter is optional.</span></span>

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

### <span data-ttu-id="d9bbb-150">– Skriv</span><span class="sxs-lookup"><span data-stu-id="d9bbb-150">-Type</span></span>
<span data-ttu-id="d9bbb-151">Identifierare för en befintlig identitets leverantör.</span><span class="sxs-lookup"><span data-stu-id="d9bbb-151">Identifier of an existing Identity Provider.</span></span>
<span data-ttu-id="d9bbb-152">Denna parameter är obligatorisk.</span><span class="sxs-lookup"><span data-stu-id="d9bbb-152">This parameter is required.</span></span>

```yaml
Type: Microsoft.Azure.Commands.ApiManagement.ServiceManagement.Models.PsApiManagementIdentityProviderType
Parameter Sets: ExpandedParameter
Aliases:
Accepted values: Facebook, Google, Microsoft, Twitter, Aad, AadB2C

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="d9bbb-153">-SigninTenant</span><span class="sxs-lookup"><span data-stu-id="d9bbb-153">-SigninTenant</span></span>
<span data-ttu-id="d9bbb-154">Logga in klient organisationen för att åsidosätta i AAD B2C i stället för `common` klient organisationen</span><span class="sxs-lookup"><span data-stu-id="d9bbb-154">Signin Tenant to override in AAD B2C instead of the `common` Tenant</span></span>

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

### <span data-ttu-id="d9bbb-155">-Bekräfta</span><span class="sxs-lookup"><span data-stu-id="d9bbb-155">-Confirm</span></span>
<span data-ttu-id="d9bbb-156">Du uppmanas att bekräfta innan du kör cmdleten.</span><span class="sxs-lookup"><span data-stu-id="d9bbb-156">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="d9bbb-157">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="d9bbb-157">-WhatIf</span></span>
<span data-ttu-id="d9bbb-158">Visar vad som händer om cmdleten körs.</span><span class="sxs-lookup"><span data-stu-id="d9bbb-158">Shows what would happen if the cmdlet runs.</span></span> <span data-ttu-id="d9bbb-159">Cmdleten körs inte.</span><span class="sxs-lookup"><span data-stu-id="d9bbb-159">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="d9bbb-160">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="d9bbb-160">CommonParameters</span></span>
<span data-ttu-id="d9bbb-161">Den här cmdleten har stöd för de gemensamma parametrarna:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-disvariable,-utbuffer,-PipelineVariable,-verbose,-WarningAction och-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="d9bbb-161">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="d9bbb-162">Mer information finns i [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="d9bbb-162">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="d9bbb-163">KOSTNADS</span><span class="sxs-lookup"><span data-stu-id="d9bbb-163">INPUTS</span></span>

### <span data-ttu-id="d9bbb-164">Microsoft. Azure. commands. ApiManagement. ServiceManagement. Models. PsApiManagementContext</span><span class="sxs-lookup"><span data-stu-id="d9bbb-164">Microsoft.Azure.Commands.ApiManagement.ServiceManagement.Models.PsApiManagementContext</span></span>

### <span data-ttu-id="d9bbb-165">Microsoft. Azure. commands. ApiManagement. ServiceManagement. Models. PsApiManagementIdentityProviderType</span><span class="sxs-lookup"><span data-stu-id="d9bbb-165">Microsoft.Azure.Commands.ApiManagement.ServiceManagement.Models.PsApiManagementIdentityProviderType</span></span>

### <span data-ttu-id="d9bbb-166">System. String</span><span class="sxs-lookup"><span data-stu-id="d9bbb-166">System.String</span></span>

### <span data-ttu-id="d9bbb-167">System. string []</span><span class="sxs-lookup"><span data-stu-id="d9bbb-167">System.String[]</span></span>

### <span data-ttu-id="d9bbb-168">System. Management. Automation. SwitchParameter</span><span class="sxs-lookup"><span data-stu-id="d9bbb-168">System.Management.Automation.SwitchParameter</span></span>

## <span data-ttu-id="d9bbb-169">VÄRDEN</span><span class="sxs-lookup"><span data-stu-id="d9bbb-169">OUTPUTS</span></span>

### <span data-ttu-id="d9bbb-170">Microsoft. Azure. commands. ApiManagement. ServiceManagement. Models. PsApiManagementIdentityProvider</span><span class="sxs-lookup"><span data-stu-id="d9bbb-170">Microsoft.Azure.Commands.ApiManagement.ServiceManagement.Models.PsApiManagementIdentityProvider</span></span>

## <span data-ttu-id="d9bbb-171">ANMÄRKNINGAR</span><span class="sxs-lookup"><span data-stu-id="d9bbb-171">NOTES</span></span>

## <span data-ttu-id="d9bbb-172">RELATERADE LÄNKAR</span><span class="sxs-lookup"><span data-stu-id="d9bbb-172">RELATED LINKS</span></span>

[<span data-ttu-id="d9bbb-173">New-AzApiManagementIdentityProvider</span><span class="sxs-lookup"><span data-stu-id="d9bbb-173">New-AzApiManagementIdentityProvider</span></span>](./New-AzApiManagementIdentityProvider.md)

[<span data-ttu-id="d9bbb-174">Get-AzApiManagementIdentityProvider</span><span class="sxs-lookup"><span data-stu-id="d9bbb-174">Get-AzApiManagementIdentityProvider</span></span>](./Get-AzApiManagementIdentityProvider.md)

[<span data-ttu-id="d9bbb-175">Remove-AzApiManagementIdentityProvider</span><span class="sxs-lookup"><span data-stu-id="d9bbb-175">Remove-AzApiManagementIdentityProvider</span></span>](./Remove-AzApiManagementIdentityProvider.md)
