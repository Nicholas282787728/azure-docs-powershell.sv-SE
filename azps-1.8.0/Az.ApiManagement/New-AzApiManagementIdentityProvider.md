---
external help file: Microsoft.Azure.PowerShell.Cmdlets.ApiManagement.ServiceManagement.dll-Help.xml
Module Name: Az.ApiManagement
online version: https://docs.microsoft.com/en-us/powershell/module/az.apimanagement/new-azapimanagementidentityprovider
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/ApiManagement/ApiManagement/help/New-AzApiManagementIdentityProvider.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/ApiManagement/ApiManagement/help/New-AzApiManagementIdentityProvider.md
ms.openlocfilehash: c0730053dce60dbf556ef00f522aa463ffb26601
ms.sourcegitcommit: 4d2c178cd6df9151877b08d54c1f4a228dbec9d1
ms.translationtype: MT
ms.contentlocale: sv-SE
ms.lasthandoff: 01/29/2020
ms.locfileid: "93754901"
---
# <span data-ttu-id="0bef9-101">New-AzApiManagementIdentityProvider</span><span class="sxs-lookup"><span data-stu-id="0bef9-101">New-AzApiManagementIdentityProvider</span></span>

## <span data-ttu-id="0bef9-102">Sammanfattning</span><span class="sxs-lookup"><span data-stu-id="0bef9-102">SYNOPSIS</span></span>
<span data-ttu-id="0bef9-103">Skapar en ny identitets leverantörs konfiguration.</span><span class="sxs-lookup"><span data-stu-id="0bef9-103">Creates a new Identity Provider configuration.</span></span>

## <span data-ttu-id="0bef9-104">FRÅGESYNTAXEN</span><span class="sxs-lookup"><span data-stu-id="0bef9-104">SYNTAX</span></span>

```
New-AzApiManagementIdentityProvider -Context <PsApiManagementContext>
 -Type <PsApiManagementIdentityProviderType> -ClientId <String> -ClientSecret <String>
 [-AllowedTenants <String[]>] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

## <span data-ttu-id="0bef9-105">PROBLEMBESKRIVNING</span><span class="sxs-lookup"><span data-stu-id="0bef9-105">DESCRIPTION</span></span>
<span data-ttu-id="0bef9-106">Skapar en ny identitets leverantörs konfiguration.</span><span class="sxs-lookup"><span data-stu-id="0bef9-106">Creates a new Identity Provider configuration.</span></span>

## <span data-ttu-id="0bef9-107">BESKRIVS</span><span class="sxs-lookup"><span data-stu-id="0bef9-107">EXAMPLES</span></span>

### <span data-ttu-id="0bef9-108">Exempel 1: konfigurerar Facebook som identitets leverantör för utvecklare som använder utvecklings portalen</span><span class="sxs-lookup"><span data-stu-id="0bef9-108">Example 1: Configures Facebook as an identity Provider for Developer Portal Logins</span></span>
```
PS C:\>$apimContext = New-AzApiManagementContext -ResourceGroupName "Api-Default-WestUS" -ServiceName "contoso"
PS C:\>New-AzApiManagementIdentityProvider -Context $apimContext -Type 'Facebook' -ClientId 'sdfsfwerwerw' -ClientSecret 'sdgsdfgfst43tewfewrf'
```

<span data-ttu-id="0bef9-109">Det här kommandot konfigurerar Facebook-identiteten som godkänd identitets leverantör på Developer-portalen för ApiManagement-tjänsten.</span><span class="sxs-lookup"><span data-stu-id="0bef9-109">This command configures Facebook Identity as a accepted Identity Provider on the Developer Portal of the ApiManagement service.</span></span>
<span data-ttu-id="0bef9-110">Det här kommer att ange ClientId och ClientSecret i Facebook-appen.</span><span class="sxs-lookup"><span data-stu-id="0bef9-110">This takes as input the ClientId and ClientSecret of the Facebook app.</span></span>

## <span data-ttu-id="0bef9-111">MALLPARAMETRAR</span><span class="sxs-lookup"><span data-stu-id="0bef9-111">PARAMETERS</span></span>

### <span data-ttu-id="0bef9-112">-AllowedTenants</span><span class="sxs-lookup"><span data-stu-id="0bef9-112">-AllowedTenants</span></span>
<span data-ttu-id="0bef9-113">Lista över tillåtna Azure Active Directory-klient organisationer</span><span class="sxs-lookup"><span data-stu-id="0bef9-113">List of allowed Azure Active Directory Tenants</span></span>

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

### <span data-ttu-id="0bef9-114">-ClientId</span><span class="sxs-lookup"><span data-stu-id="0bef9-114">-ClientId</span></span>
<span data-ttu-id="0bef9-115">Klient-ID för programmet i extern identitets leverantör.</span><span class="sxs-lookup"><span data-stu-id="0bef9-115">Client Id of the Application in the external Identity Provider.</span></span>
<span data-ttu-id="0bef9-116">Det är program-ID för Facebook-inloggning, klient-ID för Google-inloggning, app-ID för Microsoft.</span><span class="sxs-lookup"><span data-stu-id="0bef9-116">It is App ID for Facebook login, Client ID for Google login, App ID for Microsoft.</span></span>

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

### <span data-ttu-id="0bef9-117">-ClientSecret</span><span class="sxs-lookup"><span data-stu-id="0bef9-117">-ClientSecret</span></span>
<span data-ttu-id="0bef9-118">Klient hemlighet för programmet i extern identitets leverantör som används för att autentisera inloggningsbegäran.</span><span class="sxs-lookup"><span data-stu-id="0bef9-118">Client secret of the Application in external Identity Provider, used to authenticate login request.</span></span>
<span data-ttu-id="0bef9-119">Det är exempelvis program hemlighet för Facebook-inloggning, API-nyckel för Google-inloggning, offentlig nyckel för Microsoft.</span><span class="sxs-lookup"><span data-stu-id="0bef9-119">For example, it is App Secret for Facebook login, API Key for Google login, Public Key for Microsoft.</span></span>

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

### <span data-ttu-id="0bef9-120">-Kontext</span><span class="sxs-lookup"><span data-stu-id="0bef9-120">-Context</span></span>
<span data-ttu-id="0bef9-121">Instans av PsApiManagementContext.</span><span class="sxs-lookup"><span data-stu-id="0bef9-121">Instance of PsApiManagementContext.</span></span>
<span data-ttu-id="0bef9-122">Denna parameter är obligatorisk.</span><span class="sxs-lookup"><span data-stu-id="0bef9-122">This parameter is required.</span></span>

```yaml
Type: Microsoft.Azure.Commands.ApiManagement.ServiceManagement.Models.PsApiManagementContext
Parameter Sets: (All)
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="0bef9-123">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="0bef9-123">-DefaultProfile</span></span>
<span data-ttu-id="0bef9-124">Autentiseringsuppgifter, konto, klient organisation och abonnemang som används för kommunikation med Azure.</span><span class="sxs-lookup"><span data-stu-id="0bef9-124">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="0bef9-125">– Skriv</span><span class="sxs-lookup"><span data-stu-id="0bef9-125">-Type</span></span>
<span data-ttu-id="0bef9-126">Identifierare för en identitets leverantör.</span><span class="sxs-lookup"><span data-stu-id="0bef9-126">Identifier of a Identity Provider.</span></span>
<span data-ttu-id="0bef9-127">Om det här alternativet anges kan du hitta identitets leverantörens konfiguration enligt ID.</span><span class="sxs-lookup"><span data-stu-id="0bef9-127">If specified will try to find identity provider configuration by the identifier.</span></span>
<span data-ttu-id="0bef9-128">Denna parameter är valfri.</span><span class="sxs-lookup"><span data-stu-id="0bef9-128">This parameter is optional.</span></span>

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

### <span data-ttu-id="0bef9-129">-Bekräfta</span><span class="sxs-lookup"><span data-stu-id="0bef9-129">-Confirm</span></span>
<span data-ttu-id="0bef9-130">Du uppmanas att bekräfta innan du kör cmdleten.</span><span class="sxs-lookup"><span data-stu-id="0bef9-130">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="0bef9-131">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="0bef9-131">-WhatIf</span></span>
<span data-ttu-id="0bef9-132">Visar vad som händer om cmdleten körs.</span><span class="sxs-lookup"><span data-stu-id="0bef9-132">Shows what would happen if the cmdlet runs.</span></span> <span data-ttu-id="0bef9-133">Cmdleten körs inte.</span><span class="sxs-lookup"><span data-stu-id="0bef9-133">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="0bef9-134">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="0bef9-134">CommonParameters</span></span>
<span data-ttu-id="0bef9-135">Den här cmdleten har stöd för de gemensamma parametrarna:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-disvariable,-utbuffer,-PipelineVariable,-verbose,-WarningAction och-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="0bef9-135">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="0bef9-136">Mer information finns i about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="0bef9-136">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="0bef9-137">KOSTNADS</span><span class="sxs-lookup"><span data-stu-id="0bef9-137">INPUTS</span></span>

### <span data-ttu-id="0bef9-138">Microsoft. Azure. commands. ApiManagement. ServiceManagement. Models. PsApiManagementContext</span><span class="sxs-lookup"><span data-stu-id="0bef9-138">Microsoft.Azure.Commands.ApiManagement.ServiceManagement.Models.PsApiManagementContext</span></span>

### <span data-ttu-id="0bef9-139">Microsoft. Azure. commands. ApiManagement. ServiceManagement. Models. PsApiManagementIdentityProviderType</span><span class="sxs-lookup"><span data-stu-id="0bef9-139">Microsoft.Azure.Commands.ApiManagement.ServiceManagement.Models.PsApiManagementIdentityProviderType</span></span>

### <span data-ttu-id="0bef9-140">System. String</span><span class="sxs-lookup"><span data-stu-id="0bef9-140">System.String</span></span>

### <span data-ttu-id="0bef9-141">System. string []</span><span class="sxs-lookup"><span data-stu-id="0bef9-141">System.String[]</span></span>

## <span data-ttu-id="0bef9-142">VÄRDEN</span><span class="sxs-lookup"><span data-stu-id="0bef9-142">OUTPUTS</span></span>

### <span data-ttu-id="0bef9-143">Microsoft. Azure. commands. ApiManagement. ServiceManagement. Models. PsApiManagementIdentityProvider</span><span class="sxs-lookup"><span data-stu-id="0bef9-143">Microsoft.Azure.Commands.ApiManagement.ServiceManagement.Models.PsApiManagementIdentityProvider</span></span>

## <span data-ttu-id="0bef9-144">ANMÄRKNINGAR</span><span class="sxs-lookup"><span data-stu-id="0bef9-144">NOTES</span></span>

## <span data-ttu-id="0bef9-145">RELATERADE LÄNKAR</span><span class="sxs-lookup"><span data-stu-id="0bef9-145">RELATED LINKS</span></span>

[<span data-ttu-id="0bef9-146">Get-AzApiManagementIdentityProvider</span><span class="sxs-lookup"><span data-stu-id="0bef9-146">Get-AzApiManagementIdentityProvider</span></span>](./Get-AzApiManagementIdentityProvider.md)

[<span data-ttu-id="0bef9-147">Remove-AzApiManagementIdentityProvider</span><span class="sxs-lookup"><span data-stu-id="0bef9-147">Remove-AzApiManagementIdentityProvider</span></span>](./Remove-AzApiManagementIdentityProvider.md)

[<span data-ttu-id="0bef9-148">Set-AzApiManagementIdentityProvider</span><span class="sxs-lookup"><span data-stu-id="0bef9-148">Set-AzApiManagementIdentityProvider</span></span>](./Set-AzApiManagementIdentityProvider.md)
