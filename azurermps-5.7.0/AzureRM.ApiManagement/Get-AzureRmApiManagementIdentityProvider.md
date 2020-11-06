---
external help file: Microsoft.Azure.Commands.ApiManagement.ServiceManagement.dll-Help.xml
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.apimanagement/get-azurermapimanagementidentityprovider
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/ApiManagement/Commands.ApiManagement/help/Get-AzureRmApiManagementIdentityProvider.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/ApiManagement/Commands.ApiManagement/help/Get-AzureRmApiManagementIdentityProvider.md
ms.openlocfilehash: e25e3bfad6c40b136c3cbaa65999b8118e0abd11
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: sv-SE
ms.lasthandoff: 08/20/2020
ms.locfileid: "93581211"
---
# <span data-ttu-id="63feb-101">Get-AzureRmApiManagementIdentityProvider</span><span class="sxs-lookup"><span data-stu-id="63feb-101">Get-AzureRmApiManagementIdentityProvider</span></span>

## <span data-ttu-id="63feb-102">Sammanfattning</span><span class="sxs-lookup"><span data-stu-id="63feb-102">SYNOPSIS</span></span>
<span data-ttu-id="63feb-103">Hämta information om identitets leverantörens konfiguration.</span><span class="sxs-lookup"><span data-stu-id="63feb-103">Get the identity provider configuration details.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="63feb-104">FRÅGESYNTAXEN</span><span class="sxs-lookup"><span data-stu-id="63feb-104">SYNTAX</span></span>

### <span data-ttu-id="63feb-105">AllIdentityProviders (standard)</span><span class="sxs-lookup"><span data-stu-id="63feb-105">AllIdentityProviders (Default)</span></span>
```
Get-AzureRmApiManagementIdentityProvider -Context <PsApiManagementContext>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="63feb-106">IdentityProviderByType</span><span class="sxs-lookup"><span data-stu-id="63feb-106">IdentityProviderByType</span></span>
```
Get-AzureRmApiManagementIdentityProvider -Context <PsApiManagementContext>
 -Type <PsApiManagementIdentityProviderType> [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="63feb-107">PROBLEMBESKRIVNING</span><span class="sxs-lookup"><span data-stu-id="63feb-107">DESCRIPTION</span></span>
<span data-ttu-id="63feb-108">Hämta information om identitets leverantörens konfiguration.</span><span class="sxs-lookup"><span data-stu-id="63feb-108">Get the identity provider configuration details.</span></span>

## <span data-ttu-id="63feb-109">BESKRIVS</span><span class="sxs-lookup"><span data-stu-id="63feb-109">EXAMPLES</span></span>

### <span data-ttu-id="63feb-110">Exempel 1: skaffa alla identitets leverantörer</span><span class="sxs-lookup"><span data-stu-id="63feb-110">Example 1: Get all Identity Providers</span></span>

```
PS C:\>$apimContext = New-AzureRmApiManagementContext -ResourceGroupName "Api-Default-WestUS" -ServiceName "contoso"
PS C:\>Get-AzureRmApiManagementIdentityProvider -Context $apimContext
```

<span data-ttu-id="63feb-111">Få all konfigurering av identitetsprovider på tjänsten.</span><span class="sxs-lookup"><span data-stu-id="63feb-111">Get all the identity provider Configuration on the service.</span></span>

### <span data-ttu-id="63feb-112">Hämta ID för AAD-typ</span><span class="sxs-lookup"><span data-stu-id="63feb-112">Get the AAD Type Identity Provider</span></span>
```
PS C:\>$apimContext = New-AzureRmApiManagementContext -ResourceGroupName "Api-Default-WestUS" -ServiceName "contoso"
PS C:\>Get-AzureRmApiManagementIdentityProvider -Context $apimContext -Type Aad
```

<span data-ttu-id="63feb-113">Hämtar identitets leverantörs konfigurationen för Azure Active Directory.</span><span class="sxs-lookup"><span data-stu-id="63feb-113">Gets the Identity Provider Configuration of Azure Active Directory.</span></span>

## <span data-ttu-id="63feb-114">MALLPARAMETRAR</span><span class="sxs-lookup"><span data-stu-id="63feb-114">PARAMETERS</span></span>

### <span data-ttu-id="63feb-115">-Kontext</span><span class="sxs-lookup"><span data-stu-id="63feb-115">-Context</span></span>
<span data-ttu-id="63feb-116">Instans av PsApiManagementContext.</span><span class="sxs-lookup"><span data-stu-id="63feb-116">Instance of PsApiManagementContext.</span></span>
<span data-ttu-id="63feb-117">Denna parameter är obligatorisk.</span><span class="sxs-lookup"><span data-stu-id="63feb-117">This parameter is required.</span></span>

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

### <span data-ttu-id="63feb-118">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="63feb-118">-DefaultProfile</span></span>
<span data-ttu-id="63feb-119">Autentiseringsuppgifter, konto, klient organisation och abonnemang som används för kommunikation med Azure.</span><span class="sxs-lookup"><span data-stu-id="63feb-119">The credentials, account, tenant, and subscription used for communication with azure.</span></span>
 
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

### <span data-ttu-id="63feb-120">– Skriv</span><span class="sxs-lookup"><span data-stu-id="63feb-120">-Type</span></span>
<span data-ttu-id="63feb-121">Identifierare för en identitets leverantör.</span><span class="sxs-lookup"><span data-stu-id="63feb-121">Identifier of a Identity Provider.</span></span>
<span data-ttu-id="63feb-122">Om det här alternativet anges kan du hitta identitets leverantörens konfiguration enligt ID.</span><span class="sxs-lookup"><span data-stu-id="63feb-122">If specified will try to find identity provider configuration by the identifier.</span></span>
<span data-ttu-id="63feb-123">Denna parameter är valfri.</span><span class="sxs-lookup"><span data-stu-id="63feb-123">This parameter is optional.</span></span>

```yaml
Type: PsApiManagementIdentityProviderType
Parameter Sets: IdentityProviderByType
Aliases: 
Accepted values: Facebook, Google, Microsoft, Twitter, Aad

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="63feb-124">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="63feb-124">CommonParameters</span></span>
<span data-ttu-id="63feb-125">Den här cmdleten har stöd för de gemensamma parametrarna:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-disvariable,-utbuffer,-PipelineVariable,-verbose,-WarningAction och-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="63feb-125">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="63feb-126">Mer information finns i about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="63feb-126">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="63feb-127">KOSTNADS</span><span class="sxs-lookup"><span data-stu-id="63feb-127">INPUTS</span></span>

### <span data-ttu-id="63feb-128">Ingen</span><span class="sxs-lookup"><span data-stu-id="63feb-128">None</span></span>
<span data-ttu-id="63feb-129">Denna cmdlet accepterar inte indata.</span><span class="sxs-lookup"><span data-stu-id="63feb-129">This cmdlet does not accept any input.</span></span>

## <span data-ttu-id="63feb-130">VÄRDEN</span><span class="sxs-lookup"><span data-stu-id="63feb-130">OUTPUTS</span></span>

### <span data-ttu-id="63feb-131">Microsoft. Azure. commands. ApiManagement. ServiceManagement. Models. PsApiManagementIdentityProvider</span><span class="sxs-lookup"><span data-stu-id="63feb-131">Microsoft.Azure.Commands.ApiManagement.ServiceManagement.Models.PsApiManagementIdentityProvider</span></span>
<span data-ttu-id="63feb-132">Information om identitets leverantören konfigurerad i API Management Service.</span><span class="sxs-lookup"><span data-stu-id="63feb-132">The details of the Identity Provider configured in API Management service.</span></span>

### <span data-ttu-id="63feb-133">IList<Microsoft. Azure. commands. ApiManagement. ServiceManagement. Models. PsApiManagementIdentityProvider></span><span class="sxs-lookup"><span data-stu-id="63feb-133">IList<Microsoft.Azure.Commands.ApiManagement.ServiceManagement.Models.PsApiManagementIdentityProvider></span></span>
<span data-ttu-id="63feb-134">Listan över identitets leverantörer som har kon figurer ATS i API Management Service.</span><span class="sxs-lookup"><span data-stu-id="63feb-134">The list of Identity Providers configured in API Management service.</span></span>

## <span data-ttu-id="63feb-135">ANMÄRKNINGAR</span><span class="sxs-lookup"><span data-stu-id="63feb-135">NOTES</span></span>

## <span data-ttu-id="63feb-136">RELATERADE LÄNKAR</span><span class="sxs-lookup"><span data-stu-id="63feb-136">RELATED LINKS</span></span>

