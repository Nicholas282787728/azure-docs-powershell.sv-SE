---
external help file: Microsoft.Azure.PowerShell.Cmdlets.ApiManagement.ServiceManagement.dll-Help.xml
Module Name: Az.ApiManagement
online version: https://docs.microsoft.com/en-us/powershell/module/az.apimanagement/set-azapimanagementidentityprovider
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/ApiManagement/ApiManagement/help/Set-AzApiManagementIdentityProvider.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/ApiManagement/ApiManagement/help/Set-AzApiManagementIdentityProvider.md
ms.openlocfilehash: f8bc49e4a5b4e8e7fb6285327cf4432cd0561506
ms.sourcegitcommit: 4d2c178cd6df9151877b08d54c1f4a228dbec9d1
ms.translationtype: MT
ms.contentlocale: sv-SE
ms.lasthandoff: 01/29/2020
ms.locfileid: "93917689"
---
# <span data-ttu-id="4da1e-101">Set-AzApiManagementIdentityProvider</span><span class="sxs-lookup"><span data-stu-id="4da1e-101">Set-AzApiManagementIdentityProvider</span></span>

## <span data-ttu-id="4da1e-102">Sammanfattning</span><span class="sxs-lookup"><span data-stu-id="4da1e-102">SYNOPSIS</span></span>
<span data-ttu-id="4da1e-103">Uppdaterar konfigurationen för en befintlig identitets leverantör.</span><span class="sxs-lookup"><span data-stu-id="4da1e-103">Updates the Configuration of an existing Identity Provider.</span></span>

## <span data-ttu-id="4da1e-104">FRÅGESYNTAXEN</span><span class="sxs-lookup"><span data-stu-id="4da1e-104">SYNTAX</span></span>

```
Set-AzApiManagementIdentityProvider -Context <PsApiManagementContext>
 -Type <PsApiManagementIdentityProviderType> [-ClientId <String>] [-ClientSecret <String>]
 [-AllowedTenants <String[]>] [-PassThru] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

## <span data-ttu-id="4da1e-105">PROBLEMBESKRIVNING</span><span class="sxs-lookup"><span data-stu-id="4da1e-105">DESCRIPTION</span></span>
<span data-ttu-id="4da1e-106">Uppdaterar konfigurationen för en befintlig identitets leverantör.</span><span class="sxs-lookup"><span data-stu-id="4da1e-106">Updates the Configuration of an existing Identity Provider.</span></span>

## <span data-ttu-id="4da1e-107">BESKRIVS</span><span class="sxs-lookup"><span data-stu-id="4da1e-107">EXAMPLES</span></span>

### <span data-ttu-id="4da1e-108">Exempel 1</span><span class="sxs-lookup"><span data-stu-id="4da1e-108">Example 1</span></span>
```powershell
PS C:\>$apimContext = New-AzApiManagementContext -ResourceGroupName "Api-Default-WestUS" -ServiceName "contoso"
PS C:\> Set-AzApiManagementIdentityProvider -Context $apimContext -Type Facebook -ClientSecret "updatedSecret" -PassThru
```

<span data-ttu-id="4da1e-109">Cmdleten uppdaterar Facebook-identitets leverantörens klient hemlighet;</span><span class="sxs-lookup"><span data-stu-id="4da1e-109">The cmdlet updates the Client Secret of the Facebook Identity Provider;</span></span>

## <span data-ttu-id="4da1e-110">MALLPARAMETRAR</span><span class="sxs-lookup"><span data-stu-id="4da1e-110">PARAMETERS</span></span>

### <span data-ttu-id="4da1e-111">-AllowedTenants</span><span class="sxs-lookup"><span data-stu-id="4da1e-111">-AllowedTenants</span></span>
<span data-ttu-id="4da1e-112">Lista över tillåtna Azure Active Directory-klient organisationer.</span><span class="sxs-lookup"><span data-stu-id="4da1e-112">List of allowed Azure Active Directory Tenants.</span></span>

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

### <span data-ttu-id="4da1e-113">-ClientId</span><span class="sxs-lookup"><span data-stu-id="4da1e-113">-ClientId</span></span>
<span data-ttu-id="4da1e-114">Klient-ID för programmet i extern identitets leverantör.</span><span class="sxs-lookup"><span data-stu-id="4da1e-114">Client Id of the Application in the external Identity Provider.</span></span>
<span data-ttu-id="4da1e-115">Det är program-ID för Facebook-inloggning, klient-ID för Google-inloggning, app-ID för Microsoft.</span><span class="sxs-lookup"><span data-stu-id="4da1e-115">It is App ID for Facebook login, Client ID for Google login, App ID for Microsoft.</span></span>

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

### <span data-ttu-id="4da1e-116">-ClientSecret</span><span class="sxs-lookup"><span data-stu-id="4da1e-116">-ClientSecret</span></span>
<span data-ttu-id="4da1e-117">Klient hemlighet för programmet i extern identitets leverantör som används för att autentisera inloggningsbegäran.</span><span class="sxs-lookup"><span data-stu-id="4da1e-117">Client secret of the Application in external Identity Provider, used to authenticate login request.</span></span>
<span data-ttu-id="4da1e-118">Det är exempelvis program hemlighet för Facebook-inloggning, API-nyckel för Google-inloggning, offentlig nyckel för Microsoft.</span><span class="sxs-lookup"><span data-stu-id="4da1e-118">For example, it is App Secret for Facebook login, API Key for Google login, Public Key for Microsoft.</span></span>

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

### <span data-ttu-id="4da1e-119">-Kontext</span><span class="sxs-lookup"><span data-stu-id="4da1e-119">-Context</span></span>
<span data-ttu-id="4da1e-120">Instans av PsApiManagementContext.</span><span class="sxs-lookup"><span data-stu-id="4da1e-120">Instance of PsApiManagementContext.</span></span>
<span data-ttu-id="4da1e-121">Denna parameter är obligatorisk.</span><span class="sxs-lookup"><span data-stu-id="4da1e-121">This parameter is required.</span></span>

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

### <span data-ttu-id="4da1e-122">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="4da1e-122">-DefaultProfile</span></span>
<span data-ttu-id="4da1e-123">Autentiseringsuppgifter, konto, klient organisation och abonnemang som används för kommunikation med Azure.</span><span class="sxs-lookup"><span data-stu-id="4da1e-123">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="4da1e-124">-PassThru</span><span class="sxs-lookup"><span data-stu-id="4da1e-124">-PassThru</span></span>
<span data-ttu-id="4da1e-125">Anger att denna cmdlet returnerar  **PsApiManagementIdentityProvider** som denna cmdlet ändrar.</span><span class="sxs-lookup"><span data-stu-id="4da1e-125">Indicates that this cmdlet returns the  **PsApiManagementIdentityProvider** that this cmdlet modifies.</span></span>

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

### <span data-ttu-id="4da1e-126">– Skriv</span><span class="sxs-lookup"><span data-stu-id="4da1e-126">-Type</span></span>
<span data-ttu-id="4da1e-127">Identifierare för en befintlig identitets leverantör.</span><span class="sxs-lookup"><span data-stu-id="4da1e-127">Identifier of an existing Identity Provider.</span></span>
<span data-ttu-id="4da1e-128">Denna parameter är obligatorisk.</span><span class="sxs-lookup"><span data-stu-id="4da1e-128">This parameter is required.</span></span>

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

### <span data-ttu-id="4da1e-129">-Bekräfta</span><span class="sxs-lookup"><span data-stu-id="4da1e-129">-Confirm</span></span>
<span data-ttu-id="4da1e-130">Du uppmanas att bekräfta innan du kör cmdleten.</span><span class="sxs-lookup"><span data-stu-id="4da1e-130">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="4da1e-131">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="4da1e-131">-WhatIf</span></span>
<span data-ttu-id="4da1e-132">Visar vad som händer om cmdleten körs.</span><span class="sxs-lookup"><span data-stu-id="4da1e-132">Shows what would happen if the cmdlet runs.</span></span> <span data-ttu-id="4da1e-133">Cmdleten körs inte.</span><span class="sxs-lookup"><span data-stu-id="4da1e-133">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="4da1e-134">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="4da1e-134">CommonParameters</span></span>
<span data-ttu-id="4da1e-135">Den här cmdleten har stöd för de gemensamma parametrarna:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-disvariable,-utbuffer,-PipelineVariable,-verbose,-WarningAction och-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="4da1e-135">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="4da1e-136">Mer information finns i about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="4da1e-136">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="4da1e-137">KOSTNADS</span><span class="sxs-lookup"><span data-stu-id="4da1e-137">INPUTS</span></span>

### <span data-ttu-id="4da1e-138">Microsoft. Azure. commands. ApiManagement. ServiceManagement. Models. PsApiManagementContext</span><span class="sxs-lookup"><span data-stu-id="4da1e-138">Microsoft.Azure.Commands.ApiManagement.ServiceManagement.Models.PsApiManagementContext</span></span>

### <span data-ttu-id="4da1e-139">Microsoft. Azure. commands. ApiManagement. ServiceManagement. Models. PsApiManagementIdentityProviderType</span><span class="sxs-lookup"><span data-stu-id="4da1e-139">Microsoft.Azure.Commands.ApiManagement.ServiceManagement.Models.PsApiManagementIdentityProviderType</span></span>

### <span data-ttu-id="4da1e-140">System. String</span><span class="sxs-lookup"><span data-stu-id="4da1e-140">System.String</span></span>

### <span data-ttu-id="4da1e-141">System. string []</span><span class="sxs-lookup"><span data-stu-id="4da1e-141">System.String[]</span></span>

### <span data-ttu-id="4da1e-142">System. Management. Automation. SwitchParameter</span><span class="sxs-lookup"><span data-stu-id="4da1e-142">System.Management.Automation.SwitchParameter</span></span>

## <span data-ttu-id="4da1e-143">VÄRDEN</span><span class="sxs-lookup"><span data-stu-id="4da1e-143">OUTPUTS</span></span>

### <span data-ttu-id="4da1e-144">Microsoft. Azure. commands. ApiManagement. ServiceManagement. Models. PsApiManagementIdentityProvider</span><span class="sxs-lookup"><span data-stu-id="4da1e-144">Microsoft.Azure.Commands.ApiManagement.ServiceManagement.Models.PsApiManagementIdentityProvider</span></span>

## <span data-ttu-id="4da1e-145">ANMÄRKNINGAR</span><span class="sxs-lookup"><span data-stu-id="4da1e-145">NOTES</span></span>

## <span data-ttu-id="4da1e-146">RELATERADE LÄNKAR</span><span class="sxs-lookup"><span data-stu-id="4da1e-146">RELATED LINKS</span></span>

[<span data-ttu-id="4da1e-147">New-AzApiManagementIdentityProvider</span><span class="sxs-lookup"><span data-stu-id="4da1e-147">New-AzApiManagementIdentityProvider</span></span>](./New-AzApiManagementIdentityProvider.md)

[<span data-ttu-id="4da1e-148">Get-AzApiManagementIdentityProvider</span><span class="sxs-lookup"><span data-stu-id="4da1e-148">Get-AzApiManagementIdentityProvider</span></span>](./Get-AzApiManagementIdentityProvider.md)

[<span data-ttu-id="4da1e-149">Remove-AzApiManagementIdentityProvider</span><span class="sxs-lookup"><span data-stu-id="4da1e-149">Remove-AzApiManagementIdentityProvider</span></span>](./Remove-AzApiManagementIdentityProvider.md)
