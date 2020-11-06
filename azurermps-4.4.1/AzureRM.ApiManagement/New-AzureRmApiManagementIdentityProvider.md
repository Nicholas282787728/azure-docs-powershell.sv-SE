---
external help file: Microsoft.Azure.Commands.ApiManagement.ServiceManagement.dll-Help.xml
Module Name: AzureRM.ApiManagement
online version: ''
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/ApiManagement/Commands.ApiManagement/help/New-AzureRmApiManagementIdentityProvider.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/ApiManagement/Commands.ApiManagement/help/New-AzureRmApiManagementIdentityProvider.md
ms.openlocfilehash: d6536c63ab3241e999c87dfb025205571c29596c
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: sv-SE
ms.lasthandoff: 08/20/2020
ms.locfileid: "93578627"
---
# <span data-ttu-id="0469f-101">New-AzureRmApiManagementIdentityProvider</span><span class="sxs-lookup"><span data-stu-id="0469f-101">New-AzureRmApiManagementIdentityProvider</span></span>

## <span data-ttu-id="0469f-102">Sammanfattning</span><span class="sxs-lookup"><span data-stu-id="0469f-102">SYNOPSIS</span></span>
<span data-ttu-id="0469f-103">Skapar en ny identitets leverantörs konfiguration.</span><span class="sxs-lookup"><span data-stu-id="0469f-103">Creates a new Identity Provider configuration.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="0469f-104">FRÅGESYNTAXEN</span><span class="sxs-lookup"><span data-stu-id="0469f-104">SYNTAX</span></span>

```
New-AzureRmApiManagementIdentityProvider -Context <PsApiManagementContext>
 -Type <PsApiManagementIdentityProviderType> -ClientId <String> -ClientSecret <String>
 [-AllowedTenants <String[]>] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

## <span data-ttu-id="0469f-105">PROBLEMBESKRIVNING</span><span class="sxs-lookup"><span data-stu-id="0469f-105">DESCRIPTION</span></span>
<span data-ttu-id="0469f-106">Skapar en ny identitets leverantörs konfiguration.</span><span class="sxs-lookup"><span data-stu-id="0469f-106">Creates a new Identity Provider configuration.</span></span>

## <span data-ttu-id="0469f-107">BESKRIVS</span><span class="sxs-lookup"><span data-stu-id="0469f-107">EXAMPLES</span></span>

### <span data-ttu-id="0469f-108">Exempel 1: konfigurerar Facebook som identitets leverantör för utvecklare som använder utvecklings portalen</span><span class="sxs-lookup"><span data-stu-id="0469f-108">Example 1: Configures Facebook as an identity Provider for Developer Portal Logins</span></span>
```
New-AzureRmApiManagementIdentityProvider -Context $apimContext -Type 'Facebook' -ClientId 'sdfsfwerwerw' -ClientSecret 'sdgsdfgfst43tewfewrf'
```

<span data-ttu-id="0469f-109">Det här kommandot konfigurerar Facebook-identiteten som godkänd identitets leverantör på Developer-portalen för ApiManagement-tjänsten.</span><span class="sxs-lookup"><span data-stu-id="0469f-109">This command configures Facebook Identity as a accepted Identity Provider on the Developer Portal of the ApiManagement service.</span></span>
<span data-ttu-id="0469f-110">Det här kommer att ange ClientId och ClientSecret i Facebook-appen.</span><span class="sxs-lookup"><span data-stu-id="0469f-110">This takes as input the ClientId and ClientSecret of the Facebook app.</span></span>

## <span data-ttu-id="0469f-111">MALLPARAMETRAR</span><span class="sxs-lookup"><span data-stu-id="0469f-111">PARAMETERS</span></span>

### <span data-ttu-id="0469f-112">-AllowedTenants</span><span class="sxs-lookup"><span data-stu-id="0469f-112">-AllowedTenants</span></span>
<span data-ttu-id="0469f-113">Lista över tillåtna Azure Active Directory-klient organisationer</span><span class="sxs-lookup"><span data-stu-id="0469f-113">List of allowed Azure Active Directory Tenants</span></span>

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

### <span data-ttu-id="0469f-114">-ClientId</span><span class="sxs-lookup"><span data-stu-id="0469f-114">-ClientId</span></span>
<span data-ttu-id="0469f-115">Klient-ID för programmet i extern identitets leverantör.</span><span class="sxs-lookup"><span data-stu-id="0469f-115">Client Id of the Application in the external Identity Provider.</span></span>
<span data-ttu-id="0469f-116">Det är program-ID för Facebook-inloggning, klient-ID för Google-inloggning, app-ID för Microsoft.</span><span class="sxs-lookup"><span data-stu-id="0469f-116">It is App ID for Facebook login, Client ID for Google login, App ID for Microsoft.</span></span>

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

### <span data-ttu-id="0469f-117">-ClientSecret</span><span class="sxs-lookup"><span data-stu-id="0469f-117">-ClientSecret</span></span>
<span data-ttu-id="0469f-118">Klient hemlighet för programmet i extern identitets leverantör som används för att autentisera inloggningsbegäran.</span><span class="sxs-lookup"><span data-stu-id="0469f-118">Client secret of the Application in external Identity Provider, used to authenticate login request.</span></span>
<span data-ttu-id="0469f-119">Det är exempelvis program hemlighet för Facebook-inloggning, API-nyckel för Google-inloggning, offentlig nyckel för Microsoft.</span><span class="sxs-lookup"><span data-stu-id="0469f-119">For example, it is App Secret for Facebook login, API Key for Google login, Public Key for Microsoft.</span></span>

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

### <span data-ttu-id="0469f-120">-Kontext</span><span class="sxs-lookup"><span data-stu-id="0469f-120">-Context</span></span>
<span data-ttu-id="0469f-121">Instans av PsApiManagementContext.</span><span class="sxs-lookup"><span data-stu-id="0469f-121">Instance of PsApiManagementContext.</span></span>
<span data-ttu-id="0469f-122">Denna parameter är obligatorisk.</span><span class="sxs-lookup"><span data-stu-id="0469f-122">This parameter is required.</span></span>

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

### <span data-ttu-id="0469f-123">– Skriv</span><span class="sxs-lookup"><span data-stu-id="0469f-123">-Type</span></span>
<span data-ttu-id="0469f-124">Identifierare för en identitets leverantör.</span><span class="sxs-lookup"><span data-stu-id="0469f-124">Identifier of a Identity Provider.</span></span>
<span data-ttu-id="0469f-125">Om det här alternativet anges kan du hitta identitets leverantörens konfiguration enligt ID.</span><span class="sxs-lookup"><span data-stu-id="0469f-125">If specified will try to find identity provider configuration by the identifier.</span></span>
<span data-ttu-id="0469f-126">Denna parameter är valfri.</span><span class="sxs-lookup"><span data-stu-id="0469f-126">This parameter is optional.</span></span>

```yaml
Type: Microsoft.Azure.Commands.ApiManagement.ServiceManagement.Models.PsApiManagementIdentityProviderType
Parameter Sets: (All)
Aliases: 
Accepted values: Facebook, Google, Microsoft, Twitter, Aad

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="0469f-127">-Bekräfta</span><span class="sxs-lookup"><span data-stu-id="0469f-127">-Confirm</span></span>
<span data-ttu-id="0469f-128">Du uppmanas att bekräfta innan du kör cmdleten.</span><span class="sxs-lookup"><span data-stu-id="0469f-128">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="0469f-129">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="0469f-129">-WhatIf</span></span>
<span data-ttu-id="0469f-130">Visar vad som händer om cmdleten körs.</span><span class="sxs-lookup"><span data-stu-id="0469f-130">Shows what would happen if the cmdlet runs.</span></span> <span data-ttu-id="0469f-131">Cmdleten körs inte.</span><span class="sxs-lookup"><span data-stu-id="0469f-131">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="0469f-132">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="0469f-132">-DefaultProfile</span></span>
<span data-ttu-id="0469f-133">Autentiseringsuppgifter, konto, klient organisation och abonnemang som används för kommunikation med Azure.</span><span class="sxs-lookup"><span data-stu-id="0469f-133">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="0469f-134">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="0469f-134">CommonParameters</span></span>
<span data-ttu-id="0469f-135">Den här cmdleten har stöd för de gemensamma parametrarna:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-disvariable,-utbuffer,-PipelineVariable,-verbose,-WarningAction och-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="0469f-135">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="0469f-136">Mer information finns i about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="0469f-136">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="0469f-137">KOSTNADS</span><span class="sxs-lookup"><span data-stu-id="0469f-137">INPUTS</span></span>

## <span data-ttu-id="0469f-138">VÄRDEN</span><span class="sxs-lookup"><span data-stu-id="0469f-138">OUTPUTS</span></span>

### <span data-ttu-id="0469f-139">Microsoft. Azure. commands. ApiManagement. ServiceManagement. Models. PsApiManagementIdentityProvider</span><span class="sxs-lookup"><span data-stu-id="0469f-139">Microsoft.Azure.Commands.ApiManagement.ServiceManagement.Models.PsApiManagementIdentityProvider</span></span>

## <span data-ttu-id="0469f-140">ANMÄRKNINGAR</span><span class="sxs-lookup"><span data-stu-id="0469f-140">NOTES</span></span>

## <span data-ttu-id="0469f-141">RELATERADE LÄNKAR</span><span class="sxs-lookup"><span data-stu-id="0469f-141">RELATED LINKS</span></span>

[<span data-ttu-id="0469f-142">Get-AzureRmApiManagementIdentityProvider</span><span class="sxs-lookup"><span data-stu-id="0469f-142">Get-AzureRmApiManagementIdentityProvider</span></span>](./Get-AzureRmApiManagementIdentityProvider.md)

[<span data-ttu-id="0469f-143">Remove-AzureRmApiManagementIdentityProvider</span><span class="sxs-lookup"><span data-stu-id="0469f-143">Remove-AzureRmApiManagementIdentityProvider</span></span>](./Remove-AzureRmApiManagementIdentityProvider.md)

[<span data-ttu-id="0469f-144">Set-AzureRmApiManagementIdentityProvider</span><span class="sxs-lookup"><span data-stu-id="0469f-144">Set-AzureRmApiManagementIdentityProvider</span></span>](./Set-AzureRmApiManagementIdentityProvider.md)
