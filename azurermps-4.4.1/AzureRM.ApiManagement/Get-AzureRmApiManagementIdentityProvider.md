---
external help file: Microsoft.Azure.Commands.ApiManagement.ServiceManagement.dll-Help.xml
Module Name: AzureRM.ApiManagement
online version: ''
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/ApiManagement/Commands.ApiManagement/help/Get-AzureRmApiManagementIdentityProvider.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/ApiManagement/Commands.ApiManagement/help/Get-AzureRmApiManagementIdentityProvider.md
ms.openlocfilehash: 2b38728f90de4639bf3e125f226ae2b40527ca45
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: sv-SE
ms.lasthandoff: 08/20/2020
ms.locfileid: "93578692"
---
# <span data-ttu-id="18ecb-101">Get-AzureRmApiManagementIdentityProvider</span><span class="sxs-lookup"><span data-stu-id="18ecb-101">Get-AzureRmApiManagementIdentityProvider</span></span>

## <span data-ttu-id="18ecb-102">Sammanfattning</span><span class="sxs-lookup"><span data-stu-id="18ecb-102">SYNOPSIS</span></span>
<span data-ttu-id="18ecb-103">Hämta information om identitets leverantörens konfiguration.</span><span class="sxs-lookup"><span data-stu-id="18ecb-103">Get the identity provider configuration details.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="18ecb-104">FRÅGESYNTAXEN</span><span class="sxs-lookup"><span data-stu-id="18ecb-104">SYNTAX</span></span>

### <span data-ttu-id="18ecb-105">AllIdentityProviders (standard)</span><span class="sxs-lookup"><span data-stu-id="18ecb-105">AllIdentityProviders (Default)</span></span>
```
Get-AzureRmApiManagementIdentityProvider -Context <PsApiManagementContext>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="18ecb-106">IdentityProviderByType</span><span class="sxs-lookup"><span data-stu-id="18ecb-106">IdentityProviderByType</span></span>
```
Get-AzureRmApiManagementIdentityProvider -Context <PsApiManagementContext>
 -Type <PsApiManagementIdentityProviderType> [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="18ecb-107">PROBLEMBESKRIVNING</span><span class="sxs-lookup"><span data-stu-id="18ecb-107">DESCRIPTION</span></span>
<span data-ttu-id="18ecb-108">Hämta information om identitets leverantörens konfiguration.</span><span class="sxs-lookup"><span data-stu-id="18ecb-108">Get the identity provider configuration details.</span></span>

## <span data-ttu-id="18ecb-109">BESKRIVS</span><span class="sxs-lookup"><span data-stu-id="18ecb-109">EXAMPLES</span></span>

### <span data-ttu-id="18ecb-110">--------------------------Exempel 1--------------------------</span><span class="sxs-lookup"><span data-stu-id="18ecb-110">--------------------------  Example 1  --------------------------</span></span>
<span data-ttu-id="18ecb-111">@ {paragraf = PS C: \\ \> }</span><span class="sxs-lookup"><span data-stu-id="18ecb-111">@{paragraph=PS C:\\\>}</span></span>







```
Get-AzureRmApiManagementIdentityProvider -Context $context
```

<span data-ttu-id="18ecb-112">Få all konfigurering av identitetsprovider på tjänsten.</span><span class="sxs-lookup"><span data-stu-id="18ecb-112">Get all the identity provider Configuration on the service.</span></span>

### <span data-ttu-id="18ecb-113">--------------------------Exempel 2--------------------------</span><span class="sxs-lookup"><span data-stu-id="18ecb-113">--------------------------  Example 2  --------------------------</span></span>
<span data-ttu-id="18ecb-114">@ {paragraf = PS C: \\ \> }</span><span class="sxs-lookup"><span data-stu-id="18ecb-114">@{paragraph=PS C:\\\>}</span></span>







```
Get-AzureRmApiManagementIdentityProvider -Context $context -Type Aad
```

<span data-ttu-id="18ecb-115">Hämtar identitets leverantörs konfigurationen för Azure Active Directory.</span><span class="sxs-lookup"><span data-stu-id="18ecb-115">Gets the Identity Provider Configuration of Azure Active Directory.</span></span>

## <span data-ttu-id="18ecb-116">MALLPARAMETRAR</span><span class="sxs-lookup"><span data-stu-id="18ecb-116">PARAMETERS</span></span>

### <span data-ttu-id="18ecb-117">-Kontext</span><span class="sxs-lookup"><span data-stu-id="18ecb-117">-Context</span></span>
<span data-ttu-id="18ecb-118">Instans av PsApiManagementContext.</span><span class="sxs-lookup"><span data-stu-id="18ecb-118">Instance of PsApiManagementContext.</span></span>
<span data-ttu-id="18ecb-119">Denna parameter är obligatorisk.</span><span class="sxs-lookup"><span data-stu-id="18ecb-119">This parameter is required.</span></span>

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

### <span data-ttu-id="18ecb-120">– Skriv</span><span class="sxs-lookup"><span data-stu-id="18ecb-120">-Type</span></span>
<span data-ttu-id="18ecb-121">Identifierare för en identitets leverantör.</span><span class="sxs-lookup"><span data-stu-id="18ecb-121">Identifier of a Identity Provider.</span></span>
<span data-ttu-id="18ecb-122">Om det här alternativet anges kan du hitta identitets leverantörens konfiguration enligt ID.</span><span class="sxs-lookup"><span data-stu-id="18ecb-122">If specified will try to find identity provider configuration by the identifier.</span></span>
<span data-ttu-id="18ecb-123">Denna parameter är valfri.</span><span class="sxs-lookup"><span data-stu-id="18ecb-123">This parameter is optional.</span></span>

```yaml
Type: Microsoft.Azure.Commands.ApiManagement.ServiceManagement.Models.PsApiManagementIdentityProviderType
Parameter Sets: IdentityProviderByType
Aliases: 
Accepted values: Facebook, Google, Microsoft, Twitter, Aad

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="18ecb-124">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="18ecb-124">-DefaultProfile</span></span>
<span data-ttu-id="18ecb-125">Autentiseringsuppgifter, konto, klient organisation och abonnemang som används för kommunikation med Azure.</span><span class="sxs-lookup"><span data-stu-id="18ecb-125">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="18ecb-126">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="18ecb-126">CommonParameters</span></span>
<span data-ttu-id="18ecb-127">Den här cmdleten har stöd för de gemensamma parametrarna:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-disvariable,-utbuffer,-PipelineVariable,-verbose,-WarningAction och-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="18ecb-127">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="18ecb-128">Mer information finns i about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="18ecb-128">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="18ecb-129">KOSTNADS</span><span class="sxs-lookup"><span data-stu-id="18ecb-129">INPUTS</span></span>

## <span data-ttu-id="18ecb-130">VÄRDEN</span><span class="sxs-lookup"><span data-stu-id="18ecb-130">OUTPUTS</span></span>

### <span data-ttu-id="18ecb-131">IList<Microsoft. Azure. commands. ApiManagement. ServiceManagement. Models. PsApiManagementIdentityProvider></span><span class="sxs-lookup"><span data-stu-id="18ecb-131">IList<Microsoft.Azure.Commands.ApiManagement.ServiceManagement.Models.PsApiManagementIdentityProvider></span></span>

### <span data-ttu-id="18ecb-132">Microsoft. Azure. commands. ApiManagement. ServiceManagement. Models. PsApiManagementIdentityProvider</span><span class="sxs-lookup"><span data-stu-id="18ecb-132">Microsoft.Azure.Commands.ApiManagement.ServiceManagement.Models.PsApiManagementIdentityProvider</span></span>

## <span data-ttu-id="18ecb-133">ANMÄRKNINGAR</span><span class="sxs-lookup"><span data-stu-id="18ecb-133">NOTES</span></span>

## <span data-ttu-id="18ecb-134">RELATERADE LÄNKAR</span><span class="sxs-lookup"><span data-stu-id="18ecb-134">RELATED LINKS</span></span>

