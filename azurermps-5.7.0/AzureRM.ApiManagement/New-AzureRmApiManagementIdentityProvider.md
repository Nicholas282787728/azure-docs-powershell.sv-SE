---
external help file: Microsoft.Azure.Commands.ApiManagement.ServiceManagement.dll-Help.xml
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.apimanagement/new-azurermapimanagementidentityprovider
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/ApiManagement/Commands.ApiManagement/help/New-AzureRmApiManagementIdentityProvider.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/ApiManagement/Commands.ApiManagement/help/New-AzureRmApiManagementIdentityProvider.md
ms.openlocfilehash: 470692c946175c75bf21bd613e6bbf3590854768
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: sv-SE
ms.lasthandoff: 08/20/2020
ms.locfileid: "93755781"
---
# <span data-ttu-id="ea9e7-101">New-AzureRmApiManagementIdentityProvider</span><span class="sxs-lookup"><span data-stu-id="ea9e7-101">New-AzureRmApiManagementIdentityProvider</span></span>

## <span data-ttu-id="ea9e7-102">Sammanfattning</span><span class="sxs-lookup"><span data-stu-id="ea9e7-102">SYNOPSIS</span></span>
<span data-ttu-id="ea9e7-103">Skapar en ny identitets leverantörs konfiguration.</span><span class="sxs-lookup"><span data-stu-id="ea9e7-103">Creates a new Identity Provider configuration.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="ea9e7-104">FRÅGESYNTAXEN</span><span class="sxs-lookup"><span data-stu-id="ea9e7-104">SYNTAX</span></span>

```
New-AzureRmApiManagementIdentityProvider -Context <PsApiManagementContext>
 -Type <PsApiManagementIdentityProviderType> -ClientId <String> -ClientSecret <String>
 [-AllowedTenants <String[]>] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

## <span data-ttu-id="ea9e7-105">PROBLEMBESKRIVNING</span><span class="sxs-lookup"><span data-stu-id="ea9e7-105">DESCRIPTION</span></span>
<span data-ttu-id="ea9e7-106">Skapar en ny identitets leverantörs konfiguration.</span><span class="sxs-lookup"><span data-stu-id="ea9e7-106">Creates a new Identity Provider configuration.</span></span>

## <span data-ttu-id="ea9e7-107">BESKRIVS</span><span class="sxs-lookup"><span data-stu-id="ea9e7-107">EXAMPLES</span></span>

### <span data-ttu-id="ea9e7-108">Exempel 1: konfigurerar Facebook som identitets leverantör för utvecklare som använder utvecklings portalen</span><span class="sxs-lookup"><span data-stu-id="ea9e7-108">Example 1: Configures Facebook as an identity Provider for Developer Portal Logins</span></span>
```
PS C:\>$apimContext = New-AzureRmApiManagementContext -ResourceGroupName "Api-Default-WestUS" -ServiceName "contoso"
PS C:\>New-AzureRmApiManagementIdentityProvider -Context $apimContext -Type 'Facebook' -ClientId 'sdfsfwerwerw' -ClientSecret 'sdgsdfgfst43tewfewrf'
```

<span data-ttu-id="ea9e7-109">Det här kommandot konfigurerar Facebook-identiteten som godkänd identitets leverantör på Developer-portalen för ApiManagement-tjänsten.</span><span class="sxs-lookup"><span data-stu-id="ea9e7-109">This command configures Facebook Identity as a accepted Identity Provider on the Developer Portal of the ApiManagement service.</span></span>
<span data-ttu-id="ea9e7-110">Det här kommer att ange ClientId och ClientSecret i Facebook-appen.</span><span class="sxs-lookup"><span data-stu-id="ea9e7-110">This takes as input the ClientId and ClientSecret of the Facebook app.</span></span>

## <span data-ttu-id="ea9e7-111">MALLPARAMETRAR</span><span class="sxs-lookup"><span data-stu-id="ea9e7-111">PARAMETERS</span></span>

### <span data-ttu-id="ea9e7-112">-AllowedTenants</span><span class="sxs-lookup"><span data-stu-id="ea9e7-112">-AllowedTenants</span></span>
<span data-ttu-id="ea9e7-113">Lista över tillåtna Azure Active Directory-klient organisationer</span><span class="sxs-lookup"><span data-stu-id="ea9e7-113">List of allowed Azure Active Directory Tenants</span></span>

```yaml
Type: String[]
Parameter Sets: (All)
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="ea9e7-114">-ClientId</span><span class="sxs-lookup"><span data-stu-id="ea9e7-114">-ClientId</span></span>
<span data-ttu-id="ea9e7-115">Klient-ID för programmet i extern identitets leverantör.</span><span class="sxs-lookup"><span data-stu-id="ea9e7-115">Client Id of the Application in the external Identity Provider.</span></span>
<span data-ttu-id="ea9e7-116">Det är program-ID för Facebook-inloggning, klient-ID för Google-inloggning, app-ID för Microsoft.</span><span class="sxs-lookup"><span data-stu-id="ea9e7-116">It is App ID for Facebook login, Client ID for Google login, App ID for Microsoft.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="ea9e7-117">-ClientSecret</span><span class="sxs-lookup"><span data-stu-id="ea9e7-117">-ClientSecret</span></span>
<span data-ttu-id="ea9e7-118">Klient hemlighet för programmet i extern identitets leverantör som används för att autentisera inloggningsbegäran.</span><span class="sxs-lookup"><span data-stu-id="ea9e7-118">Client secret of the Application in external Identity Provider, used to authenticate login request.</span></span>
<span data-ttu-id="ea9e7-119">Det är exempelvis program hemlighet för Facebook-inloggning, API-nyckel för Google-inloggning, offentlig nyckel för Microsoft.</span><span class="sxs-lookup"><span data-stu-id="ea9e7-119">For example, it is App Secret for Facebook login, API Key for Google login, Public Key for Microsoft.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="ea9e7-120">-Kontext</span><span class="sxs-lookup"><span data-stu-id="ea9e7-120">-Context</span></span>
<span data-ttu-id="ea9e7-121">Instans av PsApiManagementContext.</span><span class="sxs-lookup"><span data-stu-id="ea9e7-121">Instance of PsApiManagementContext.</span></span>
<span data-ttu-id="ea9e7-122">Denna parameter är obligatorisk.</span><span class="sxs-lookup"><span data-stu-id="ea9e7-122">This parameter is required.</span></span>

```yaml
Type: PsApiManagementContext
Parameter Sets: (All)
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="ea9e7-123">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="ea9e7-123">-DefaultProfile</span></span>
<span data-ttu-id="ea9e7-124">Autentiseringsuppgifter, konto, klient organisation och abonnemang som används för kommunikation med Azure.</span><span class="sxs-lookup"><span data-stu-id="ea9e7-124">The credentials, account, tenant, and subscription used for communication with azure.</span></span>
 
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

### <span data-ttu-id="ea9e7-125">– Skriv</span><span class="sxs-lookup"><span data-stu-id="ea9e7-125">-Type</span></span>
<span data-ttu-id="ea9e7-126">Identifierare för en identitets leverantör.</span><span class="sxs-lookup"><span data-stu-id="ea9e7-126">Identifier of a Identity Provider.</span></span>
<span data-ttu-id="ea9e7-127">Om det här alternativet anges kan du hitta identitets leverantörens konfiguration enligt ID.</span><span class="sxs-lookup"><span data-stu-id="ea9e7-127">If specified will try to find identity provider configuration by the identifier.</span></span>
<span data-ttu-id="ea9e7-128">Denna parameter är valfri.</span><span class="sxs-lookup"><span data-stu-id="ea9e7-128">This parameter is optional.</span></span>

```yaml
Type: PsApiManagementIdentityProviderType
Parameter Sets: (All)
Aliases: 
Accepted values: Facebook, Google, Microsoft, Twitter, Aad

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="ea9e7-129">-Bekräfta</span><span class="sxs-lookup"><span data-stu-id="ea9e7-129">-Confirm</span></span>
<span data-ttu-id="ea9e7-130">Du uppmanas att bekräfta innan du kör cmdleten.</span><span class="sxs-lookup"><span data-stu-id="ea9e7-130">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="ea9e7-131">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="ea9e7-131">-WhatIf</span></span>
<span data-ttu-id="ea9e7-132">Visar vad som händer om cmdleten körs.</span><span class="sxs-lookup"><span data-stu-id="ea9e7-132">Shows what would happen if the cmdlet runs.</span></span> <span data-ttu-id="ea9e7-133">Cmdleten körs inte.</span><span class="sxs-lookup"><span data-stu-id="ea9e7-133">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="ea9e7-134">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="ea9e7-134">CommonParameters</span></span>
<span data-ttu-id="ea9e7-135">Den här cmdleten har stöd för de gemensamma parametrarna:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-disvariable,-utbuffer,-PipelineVariable,-verbose,-WarningAction och-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="ea9e7-135">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="ea9e7-136">Mer information finns i about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="ea9e7-136">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="ea9e7-137">KOSTNADS</span><span class="sxs-lookup"><span data-stu-id="ea9e7-137">INPUTS</span></span>

### <span data-ttu-id="ea9e7-138">Ingen</span><span class="sxs-lookup"><span data-stu-id="ea9e7-138">None</span></span>
<span data-ttu-id="ea9e7-139">Denna cmdlet accepterar inte indata.</span><span class="sxs-lookup"><span data-stu-id="ea9e7-139">This cmdlet does not accept any input.</span></span>

## <span data-ttu-id="ea9e7-140">VÄRDEN</span><span class="sxs-lookup"><span data-stu-id="ea9e7-140">OUTPUTS</span></span>

### <span data-ttu-id="ea9e7-141">Microsoft. Azure. commands. ApiManagement. ServiceManagement. Models. PsApiManagementIdentityProvider</span><span class="sxs-lookup"><span data-stu-id="ea9e7-141">Microsoft.Azure.Commands.ApiManagement.ServiceManagement.Models.PsApiManagementIdentityProvider</span></span>

## <span data-ttu-id="ea9e7-142">ANMÄRKNINGAR</span><span class="sxs-lookup"><span data-stu-id="ea9e7-142">NOTES</span></span>

## <span data-ttu-id="ea9e7-143">RELATERADE LÄNKAR</span><span class="sxs-lookup"><span data-stu-id="ea9e7-143">RELATED LINKS</span></span>

[<span data-ttu-id="ea9e7-144">Get-AzureRmApiManagementIdentityProvider</span><span class="sxs-lookup"><span data-stu-id="ea9e7-144">Get-AzureRmApiManagementIdentityProvider</span></span>](./Get-AzureRmApiManagementIdentityProvider.md)

[<span data-ttu-id="ea9e7-145">Remove-AzureRmApiManagementIdentityProvider</span><span class="sxs-lookup"><span data-stu-id="ea9e7-145">Remove-AzureRmApiManagementIdentityProvider</span></span>](./Remove-AzureRmApiManagementIdentityProvider.md)

[<span data-ttu-id="ea9e7-146">Set-AzureRmApiManagementIdentityProvider</span><span class="sxs-lookup"><span data-stu-id="ea9e7-146">Set-AzureRmApiManagementIdentityProvider</span></span>](./Set-AzureRmApiManagementIdentityProvider.md)
