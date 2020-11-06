---
external help file: Microsoft.Azure.Commands.ApiManagement.ServiceManagement.dll-Help.xml
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.apimanagement/set-azurermapimanagementidentityprovider
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/ApiManagement/Commands.ApiManagement/help/Set-AzureRmApiManagementIdentityProvider.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/ApiManagement/Commands.ApiManagement/help/Set-AzureRmApiManagementIdentityProvider.md
ms.openlocfilehash: e45ec5a3d49bf82ab945a3ef3b41362a1e1e2bd3
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: sv-SE
ms.lasthandoff: 08/20/2020
ms.locfileid: "93585196"
---
# <span data-ttu-id="4c6cf-101">Set-AzureRmApiManagementIdentityProvider</span><span class="sxs-lookup"><span data-stu-id="4c6cf-101">Set-AzureRmApiManagementIdentityProvider</span></span>

## <span data-ttu-id="4c6cf-102">Sammanfattning</span><span class="sxs-lookup"><span data-stu-id="4c6cf-102">SYNOPSIS</span></span>
<span data-ttu-id="4c6cf-103">Uppdaterar konfigurationen för en befintlig identitets leverantör.</span><span class="sxs-lookup"><span data-stu-id="4c6cf-103">Updates the Configuration of an existing Identity Provider.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="4c6cf-104">FRÅGESYNTAXEN</span><span class="sxs-lookup"><span data-stu-id="4c6cf-104">SYNTAX</span></span>

```
Set-AzureRmApiManagementIdentityProvider -Context <PsApiManagementContext>
 -Type <PsApiManagementIdentityProviderType> [-ClientId <String>] [-ClientSecret <String>]
 [-AllowedTenants <String[]>] [-PassThru] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

## <span data-ttu-id="4c6cf-105">PROBLEMBESKRIVNING</span><span class="sxs-lookup"><span data-stu-id="4c6cf-105">DESCRIPTION</span></span>
<span data-ttu-id="4c6cf-106">Uppdaterar konfigurationen för en befintlig identitets leverantör.</span><span class="sxs-lookup"><span data-stu-id="4c6cf-106">Updates the Configuration of an existing Identity Provider.</span></span>

## <span data-ttu-id="4c6cf-107">BESKRIVS</span><span class="sxs-lookup"><span data-stu-id="4c6cf-107">EXAMPLES</span></span>

### <span data-ttu-id="4c6cf-108">Exempel 1</span><span class="sxs-lookup"><span data-stu-id="4c6cf-108">Example 1</span></span>
```
PS C:\>$apimContext = New-AzureRmApiManagementContext -ResourceGroupName "Api-Default-WestUS" -ServiceName "contoso"
PS C:\> Set-AzureRmApiManagementIdentityProvider -Context $apimContext -Type Facebook -ClientSecret "updatedSecret" -PassThru
```

<span data-ttu-id="4c6cf-109">Cmdleten uppdaterar Facebook-identitets leverantörens klient hemlighet;</span><span class="sxs-lookup"><span data-stu-id="4c6cf-109">The cmdlet updates the Client Secret of the Facebook Identity Provider;</span></span>

## <span data-ttu-id="4c6cf-110">MALLPARAMETRAR</span><span class="sxs-lookup"><span data-stu-id="4c6cf-110">PARAMETERS</span></span>

### <span data-ttu-id="4c6cf-111">-AllowedTenants</span><span class="sxs-lookup"><span data-stu-id="4c6cf-111">-AllowedTenants</span></span>
<span data-ttu-id="4c6cf-112">Lista över tillåtna Azure Active Directory-klient organisationer.</span><span class="sxs-lookup"><span data-stu-id="4c6cf-112">List of allowed Azure Active Directory Tenants.</span></span>

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

### <span data-ttu-id="4c6cf-113">-ClientId</span><span class="sxs-lookup"><span data-stu-id="4c6cf-113">-ClientId</span></span>
<span data-ttu-id="4c6cf-114">Klient-ID för programmet i extern identitets leverantör.</span><span class="sxs-lookup"><span data-stu-id="4c6cf-114">Client Id of the Application in the external Identity Provider.</span></span>
<span data-ttu-id="4c6cf-115">Det är program-ID för Facebook-inloggning, klient-ID för Google-inloggning, app-ID för Microsoft.</span><span class="sxs-lookup"><span data-stu-id="4c6cf-115">It is App ID for Facebook login, Client ID for Google login, App ID for Microsoft.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="4c6cf-116">-ClientSecret</span><span class="sxs-lookup"><span data-stu-id="4c6cf-116">-ClientSecret</span></span>
<span data-ttu-id="4c6cf-117">Klient hemlighet för programmet i extern identitets leverantör som används för att autentisera inloggningsbegäran.</span><span class="sxs-lookup"><span data-stu-id="4c6cf-117">Client secret of the Application in external Identity Provider, used to authenticate login request.</span></span>
<span data-ttu-id="4c6cf-118">Det är exempelvis program hemlighet för Facebook-inloggning, API-nyckel för Google-inloggning, offentlig nyckel för Microsoft.</span><span class="sxs-lookup"><span data-stu-id="4c6cf-118">For example, it is App Secret for Facebook login, API Key for Google login, Public Key for Microsoft.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="4c6cf-119">-Kontext</span><span class="sxs-lookup"><span data-stu-id="4c6cf-119">-Context</span></span>
<span data-ttu-id="4c6cf-120">Instans av PsApiManagementContext.</span><span class="sxs-lookup"><span data-stu-id="4c6cf-120">Instance of PsApiManagementContext.</span></span>
<span data-ttu-id="4c6cf-121">Denna parameter är obligatorisk.</span><span class="sxs-lookup"><span data-stu-id="4c6cf-121">This parameter is required.</span></span>

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

### <span data-ttu-id="4c6cf-122">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="4c6cf-122">-DefaultProfile</span></span>
<span data-ttu-id="4c6cf-123">Autentiseringsuppgifter, konto, klient organisation och abonnemang som används för kommunikation med Azure.</span><span class="sxs-lookup"><span data-stu-id="4c6cf-123">The credentials, account, tenant, and subscription used for communication with azure.</span></span>
 
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

### <span data-ttu-id="4c6cf-124">-PassThru</span><span class="sxs-lookup"><span data-stu-id="4c6cf-124">-PassThru</span></span>
<span data-ttu-id="4c6cf-125">Anger att denna cmdlet returnerar  **PsApiManagementIdentityProvider** som denna cmdlet ändrar.</span><span class="sxs-lookup"><span data-stu-id="4c6cf-125">Indicates that this cmdlet returns the  **PsApiManagementIdentityProvider** that this cmdlet modifies.</span></span>


```yaml
Type: SwitchParameter
Parameter Sets: (All)
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="4c6cf-126">– Skriv</span><span class="sxs-lookup"><span data-stu-id="4c6cf-126">-Type</span></span>
<span data-ttu-id="4c6cf-127">Identifierare för en befintlig identitets leverantör.</span><span class="sxs-lookup"><span data-stu-id="4c6cf-127">Identifier of an existing Identity Provider.</span></span>
<span data-ttu-id="4c6cf-128">Denna parameter är obligatorisk.</span><span class="sxs-lookup"><span data-stu-id="4c6cf-128">This parameter is required.</span></span>

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

### <span data-ttu-id="4c6cf-129">-Bekräfta</span><span class="sxs-lookup"><span data-stu-id="4c6cf-129">-Confirm</span></span>
<span data-ttu-id="4c6cf-130">Du uppmanas att bekräfta innan du kör cmdleten.</span><span class="sxs-lookup"><span data-stu-id="4c6cf-130">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="4c6cf-131">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="4c6cf-131">-WhatIf</span></span>
<span data-ttu-id="4c6cf-132">Visar vad som händer om cmdleten körs.</span><span class="sxs-lookup"><span data-stu-id="4c6cf-132">Shows what would happen if the cmdlet runs.</span></span> <span data-ttu-id="4c6cf-133">Cmdleten körs inte.</span><span class="sxs-lookup"><span data-stu-id="4c6cf-133">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="4c6cf-134">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="4c6cf-134">CommonParameters</span></span>
<span data-ttu-id="4c6cf-135">Den här cmdleten har stöd för de gemensamma parametrarna:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-disvariable,-utbuffer,-PipelineVariable,-verbose,-WarningAction och-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="4c6cf-135">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="4c6cf-136">Mer information finns i about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="4c6cf-136">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="4c6cf-137">KOSTNADS</span><span class="sxs-lookup"><span data-stu-id="4c6cf-137">INPUTS</span></span>

### <span data-ttu-id="4c6cf-138">Ingen</span><span class="sxs-lookup"><span data-stu-id="4c6cf-138">None</span></span>
<span data-ttu-id="4c6cf-139">Denna cmdlet accepterar inte indata.</span><span class="sxs-lookup"><span data-stu-id="4c6cf-139">This cmdlet does not accept any input.</span></span>

## <span data-ttu-id="4c6cf-140">VÄRDEN</span><span class="sxs-lookup"><span data-stu-id="4c6cf-140">OUTPUTS</span></span>

### <span data-ttu-id="4c6cf-141">Microsoft. Azure. commands. ApiManagement. ServiceManagement. Models. PsApiManagementIdentityProvider</span><span class="sxs-lookup"><span data-stu-id="4c6cf-141">Microsoft.Azure.Commands.ApiManagement.ServiceManagement.Models.PsApiManagementIdentityProvider</span></span>

## <span data-ttu-id="4c6cf-142">ANMÄRKNINGAR</span><span class="sxs-lookup"><span data-stu-id="4c6cf-142">NOTES</span></span>

## <span data-ttu-id="4c6cf-143">RELATERADE LÄNKAR</span><span class="sxs-lookup"><span data-stu-id="4c6cf-143">RELATED LINKS</span></span>

[<span data-ttu-id="4c6cf-144">New-AzureRmApiManagementIdentityProvider</span><span class="sxs-lookup"><span data-stu-id="4c6cf-144">New-AzureRmApiManagementIdentityProvider</span></span>](./New-AzureRmApiManagementIdentityProvider.md)

[<span data-ttu-id="4c6cf-145">Get-AzureRmApiManagementIdentityProvider</span><span class="sxs-lookup"><span data-stu-id="4c6cf-145">Get-AzureRmApiManagementIdentityProvider</span></span>](./Get-AzureRmApiManagementIdentityProvider.md)

[<span data-ttu-id="4c6cf-146">Remove-AzureRmApiManagementIdentityProvider</span><span class="sxs-lookup"><span data-stu-id="4c6cf-146">Remove-AzureRmApiManagementIdentityProvider</span></span>](./Remove-AzureRmApiManagementIdentityProvider.md)
