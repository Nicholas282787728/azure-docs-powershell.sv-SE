---
external help file: Microsoft.Azure.Commands.ApiManagement.ServiceManagement.dll-Help.xml
Module Name: AzureRM.ApiManagement
online version: ''
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/ApiManagement/Commands.ApiManagement/help/Set-AzureRmApiManagementIdentityProvider.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/ApiManagement/Commands.ApiManagement/help/Set-AzureRmApiManagementIdentityProvider.md
ms.openlocfilehash: 76ee402fee2e18d426875340d4eaadda2cc63042
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: sv-SE
ms.lasthandoff: 08/20/2020
ms.locfileid: "93579864"
---
# <span data-ttu-id="6ee78-101">Set-AzureRmApiManagementIdentityProvider</span><span class="sxs-lookup"><span data-stu-id="6ee78-101">Set-AzureRmApiManagementIdentityProvider</span></span>

## <span data-ttu-id="6ee78-102">Sammanfattning</span><span class="sxs-lookup"><span data-stu-id="6ee78-102">SYNOPSIS</span></span>
<span data-ttu-id="6ee78-103">Uppdaterar konfigurationen för en befintlig identitets leverantör.</span><span class="sxs-lookup"><span data-stu-id="6ee78-103">Updates the Configuration of an existing Identity Provider.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="6ee78-104">FRÅGESYNTAXEN</span><span class="sxs-lookup"><span data-stu-id="6ee78-104">SYNTAX</span></span>

```
Set-AzureRmApiManagementIdentityProvider -Context <PsApiManagementContext>
 -Type <PsApiManagementIdentityProviderType> [-ClientId <String>] [-ClientSecret <String>]
 [-AllowedTenants <String[]>] [-PassThru] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

## <span data-ttu-id="6ee78-105">PROBLEMBESKRIVNING</span><span class="sxs-lookup"><span data-stu-id="6ee78-105">DESCRIPTION</span></span>
<span data-ttu-id="6ee78-106">Uppdaterar konfigurationen för en befintlig identitets leverantör.</span><span class="sxs-lookup"><span data-stu-id="6ee78-106">Updates the Configuration of an existing Identity Provider.</span></span>

## <span data-ttu-id="6ee78-107">BESKRIVS</span><span class="sxs-lookup"><span data-stu-id="6ee78-107">EXAMPLES</span></span>

### <span data-ttu-id="6ee78-108">Exempel 1</span><span class="sxs-lookup"><span data-stu-id="6ee78-108">Example 1</span></span>
```
PS C:\> Set-AzureRmApiManagementIdentityProvider -Context $apimcontext -Type Facebook -ClientSecret "updatedSecret" -PassThru
```

<span data-ttu-id="6ee78-109">Cmdleten uppdaterar Facebook-identitets leverantörens klient hemlighet;</span><span class="sxs-lookup"><span data-stu-id="6ee78-109">The cmdlet updates the Client Secret of the Facebook Identity Provider;</span></span>

## <span data-ttu-id="6ee78-110">MALLPARAMETRAR</span><span class="sxs-lookup"><span data-stu-id="6ee78-110">PARAMETERS</span></span>

### <span data-ttu-id="6ee78-111">-AllowedTenants</span><span class="sxs-lookup"><span data-stu-id="6ee78-111">-AllowedTenants</span></span>
<span data-ttu-id="6ee78-112">Lista över tillåtna Azure Active Directory-klient organisationer.</span><span class="sxs-lookup"><span data-stu-id="6ee78-112">List of allowed Azure Active Directory Tenants.</span></span>

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

### <span data-ttu-id="6ee78-113">-ClientId</span><span class="sxs-lookup"><span data-stu-id="6ee78-113">-ClientId</span></span>
<span data-ttu-id="6ee78-114">Klient-ID för programmet i extern identitets leverantör.</span><span class="sxs-lookup"><span data-stu-id="6ee78-114">Client Id of the Application in the external Identity Provider.</span></span>
<span data-ttu-id="6ee78-115">Det är program-ID för Facebook-inloggning, klient-ID för Google-inloggning, app-ID för Microsoft.</span><span class="sxs-lookup"><span data-stu-id="6ee78-115">It is App ID for Facebook login, Client ID for Google login, App ID for Microsoft.</span></span>

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

### <span data-ttu-id="6ee78-116">-ClientSecret</span><span class="sxs-lookup"><span data-stu-id="6ee78-116">-ClientSecret</span></span>
<span data-ttu-id="6ee78-117">Klient hemlighet för programmet i extern identitets leverantör som används för att autentisera inloggningsbegäran.</span><span class="sxs-lookup"><span data-stu-id="6ee78-117">Client secret of the Application in external Identity Provider, used to authenticate login request.</span></span>
<span data-ttu-id="6ee78-118">Det är exempelvis program hemlighet för Facebook-inloggning, API-nyckel för Google-inloggning, offentlig nyckel för Microsoft.</span><span class="sxs-lookup"><span data-stu-id="6ee78-118">For example, it is App Secret for Facebook login, API Key for Google login, Public Key for Microsoft.</span></span>

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

### <span data-ttu-id="6ee78-119">-Kontext</span><span class="sxs-lookup"><span data-stu-id="6ee78-119">-Context</span></span>
<span data-ttu-id="6ee78-120">Instans av PsApiManagementContext.</span><span class="sxs-lookup"><span data-stu-id="6ee78-120">Instance of PsApiManagementContext.</span></span>
<span data-ttu-id="6ee78-121">Denna parameter är obligatorisk.</span><span class="sxs-lookup"><span data-stu-id="6ee78-121">This parameter is required.</span></span>

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

### <span data-ttu-id="6ee78-122">-PassThru</span><span class="sxs-lookup"><span data-stu-id="6ee78-122">-PassThru</span></span>
<span data-ttu-id="6ee78-123">Anger att denna cmdlet returnerar  **PsApiManagementIdentityProvider** som denna cmdlet ändrar.</span><span class="sxs-lookup"><span data-stu-id="6ee78-123">Indicates that this cmdlet returns the  **PsApiManagementIdentityProvider** that this cmdlet modifies.</span></span>


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

### <span data-ttu-id="6ee78-124">– Skriv</span><span class="sxs-lookup"><span data-stu-id="6ee78-124">-Type</span></span>
<span data-ttu-id="6ee78-125">Identifierare för en befintlig identitets leverantör.</span><span class="sxs-lookup"><span data-stu-id="6ee78-125">Identifier of an existing Identity Provider.</span></span>
<span data-ttu-id="6ee78-126">Denna parameter är obligatorisk.</span><span class="sxs-lookup"><span data-stu-id="6ee78-126">This parameter is required.</span></span>

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

### <span data-ttu-id="6ee78-127">-Bekräfta</span><span class="sxs-lookup"><span data-stu-id="6ee78-127">-Confirm</span></span>
<span data-ttu-id="6ee78-128">Du uppmanas att bekräfta innan du kör cmdleten.</span><span class="sxs-lookup"><span data-stu-id="6ee78-128">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="6ee78-129">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="6ee78-129">-WhatIf</span></span>
<span data-ttu-id="6ee78-130">Visar vad som händer om cmdleten körs.</span><span class="sxs-lookup"><span data-stu-id="6ee78-130">Shows what would happen if the cmdlet runs.</span></span> <span data-ttu-id="6ee78-131">Cmdleten körs inte.</span><span class="sxs-lookup"><span data-stu-id="6ee78-131">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="6ee78-132">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="6ee78-132">-DefaultProfile</span></span>
<span data-ttu-id="6ee78-133">Autentiseringsuppgifter, konto, klient organisation och abonnemang som används för kommunikation med Azure.</span><span class="sxs-lookup"><span data-stu-id="6ee78-133">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="6ee78-134">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="6ee78-134">CommonParameters</span></span>
<span data-ttu-id="6ee78-135">Den här cmdleten har stöd för de gemensamma parametrarna:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-disvariable,-utbuffer,-PipelineVariable,-verbose,-WarningAction och-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="6ee78-135">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="6ee78-136">Mer information finns i about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="6ee78-136">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="6ee78-137">KOSTNADS</span><span class="sxs-lookup"><span data-stu-id="6ee78-137">INPUTS</span></span>

## <span data-ttu-id="6ee78-138">VÄRDEN</span><span class="sxs-lookup"><span data-stu-id="6ee78-138">OUTPUTS</span></span>

### <span data-ttu-id="6ee78-139">Microsoft. Azure. commands. ApiManagement. ServiceManagement. Models. PsApiManagementIdentityProvider</span><span class="sxs-lookup"><span data-stu-id="6ee78-139">Microsoft.Azure.Commands.ApiManagement.ServiceManagement.Models.PsApiManagementIdentityProvider</span></span>

## <span data-ttu-id="6ee78-140">ANMÄRKNINGAR</span><span class="sxs-lookup"><span data-stu-id="6ee78-140">NOTES</span></span>

## <span data-ttu-id="6ee78-141">RELATERADE LÄNKAR</span><span class="sxs-lookup"><span data-stu-id="6ee78-141">RELATED LINKS</span></span>

[<span data-ttu-id="6ee78-142">New-AzureRmApiManagementIdentityProvider</span><span class="sxs-lookup"><span data-stu-id="6ee78-142">New-AzureRmApiManagementIdentityProvider</span></span>](./New-AzureRmApiManagementIdentityProvider.md)

[<span data-ttu-id="6ee78-143">Get-AzureRmApiManagementIdentityProvider</span><span class="sxs-lookup"><span data-stu-id="6ee78-143">Get-AzureRmApiManagementIdentityProvider</span></span>](./Get-AzureRmApiManagementIdentityProvider.md)

[<span data-ttu-id="6ee78-144">Remove-AzureRmApiManagementIdentityProvider</span><span class="sxs-lookup"><span data-stu-id="6ee78-144">Remove-AzureRmApiManagementIdentityProvider</span></span>](./Remove-AzureRmApiManagementIdentityProvider.md)
