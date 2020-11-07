---
external help file: Microsoft.Azure.Commands.ApiManagement.ServiceManagement.dll-Help.xml
Module Name: AzureRM.ApiManagement
ms.assetid: 15B6EAE2-56ED-4A01-B8EA-52B9FCDC1F66
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.apimanagement/get-azurermapimanagementopenidconnectprovider
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/ApiManagement/Commands.ApiManagement/help/Get-AzureRmApiManagementOpenIdConnectProvider.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/ApiManagement/Commands.ApiManagement/help/Get-AzureRmApiManagementOpenIdConnectProvider.md
ms.openlocfilehash: c26fb8991acc47ab655cb47c44194ca209423a70
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: sv-SE
ms.lasthandoff: 08/20/2020
ms.locfileid: "93756823"
---
# <span data-ttu-id="0ef99-101">Get-AzureRmApiManagementOpenIdConnectProvider</span><span class="sxs-lookup"><span data-stu-id="0ef99-101">Get-AzureRmApiManagementOpenIdConnectProvider</span></span>

## <span data-ttu-id="0ef99-102">Sammanfattning</span><span class="sxs-lookup"><span data-stu-id="0ef99-102">SYNOPSIS</span></span>
<span data-ttu-id="0ef99-103">Hämtar OpenID.</span><span class="sxs-lookup"><span data-stu-id="0ef99-103">Gets OpenID Connect providers.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="0ef99-104">FRÅGESYNTAXEN</span><span class="sxs-lookup"><span data-stu-id="0ef99-104">SYNTAX</span></span>

### <span data-ttu-id="0ef99-105">GetAllOpenIdConnectProviders (standard)</span><span class="sxs-lookup"><span data-stu-id="0ef99-105">GetAllOpenIdConnectProviders (Default)</span></span>
```
Get-AzureRmApiManagementOpenIdConnectProvider -Context <PsApiManagementContext>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="0ef99-106">GetByOpenIdConnectProviderId</span><span class="sxs-lookup"><span data-stu-id="0ef99-106">GetByOpenIdConnectProviderId</span></span>
```
Get-AzureRmApiManagementOpenIdConnectProvider -Context <PsApiManagementContext>
 [-OpenIdConnectProviderId <String>] [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="0ef99-107">GetByName</span><span class="sxs-lookup"><span data-stu-id="0ef99-107">GetByName</span></span>
```
Get-AzureRmApiManagementOpenIdConnectProvider -Context <PsApiManagementContext> [-Name <String>]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="0ef99-108">PROBLEMBESKRIVNING</span><span class="sxs-lookup"><span data-stu-id="0ef99-108">DESCRIPTION</span></span>
<span data-ttu-id="0ef99-109">Cmdleten **Get-AzureRmApiManagementOpenIdConnectProvider** hämtar OpenID Connect-leverantörer i Azure API Management.</span><span class="sxs-lookup"><span data-stu-id="0ef99-109">The **Get-AzureRmApiManagementOpenIdConnectProvider** cmdlet gets OpenID Connect providers in Azure API Management.</span></span>

## <span data-ttu-id="0ef99-110">BESKRIVS</span><span class="sxs-lookup"><span data-stu-id="0ef99-110">EXAMPLES</span></span>

### <span data-ttu-id="0ef99-111">Exempel 1: Hämta alla leverantörer</span><span class="sxs-lookup"><span data-stu-id="0ef99-111">Example 1: Get all providers</span></span>
```
PS C:\>$apimContext = New-AzureRmApiManagementContext -ResourceGroupName "Api-Default-WestUS" -ServiceName "contoso"
PS C:\>Get-AzureRmApiManagementOpenIdConnectProvider -Context $apimContext
```

<span data-ttu-id="0ef99-112">Det här kommandot får alla OpenID Connect-leverantörer för angiven kontext.</span><span class="sxs-lookup"><span data-stu-id="0ef99-112">This command gets all OpenID Connect providers for the specified context.</span></span>

### <span data-ttu-id="0ef99-113">Exempel 2: skaffa en leverantör med hjälp av ett ID</span><span class="sxs-lookup"><span data-stu-id="0ef99-113">Example 2: Get a provider by using an ID</span></span>
```
PS C:\>$apimContext = New-AzureRmApiManagementContext -ResourceGroupName "Api-Default-WestUS" -ServiceName "contoso"
PS C:\>Get-AzureRmApiManagementOpenIdConnectProvider -Context $apimContext -OpenIdConnectProviderId "OICProvicer01"
```

<span data-ttu-id="0ef99-114">Det här kommandot får leverantören med ID-OICProvicer01.</span><span class="sxs-lookup"><span data-stu-id="0ef99-114">This command gets the provider that has the ID OICProvicer01.</span></span>

### <span data-ttu-id="0ef99-115">Exempel 3: skaffa en leverantör genom att använda ett namn</span><span class="sxs-lookup"><span data-stu-id="0ef99-115">Example 3: Get a provider by using a name</span></span>
```
PS C:\>$apimContext = New-AzureRmApiManagementContext -ResourceGroupName "Api-Default-WestUS" -ServiceName "contoso"
PS C:\>Get-AzureRmApiManagementOpenIdConnectProvider -Context $apimContext -Name "Contoso OpenID Connect Provider"
```

<span data-ttu-id="0ef99-116">Med det här kommandot hämtas leverantören Contoso OpenID Connect-leverantör.</span><span class="sxs-lookup"><span data-stu-id="0ef99-116">This command gets the provider named Contoso OpenID Connect Provider.</span></span>

## <span data-ttu-id="0ef99-117">MALLPARAMETRAR</span><span class="sxs-lookup"><span data-stu-id="0ef99-117">PARAMETERS</span></span>

### <span data-ttu-id="0ef99-118">-Kontext</span><span class="sxs-lookup"><span data-stu-id="0ef99-118">-Context</span></span>
<span data-ttu-id="0ef99-119">Anger ett **PsApiManagementContext** -objekt.</span><span class="sxs-lookup"><span data-stu-id="0ef99-119">Specifies a **PsApiManagementContext** object.</span></span>

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

### <span data-ttu-id="0ef99-120">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="0ef99-120">-DefaultProfile</span></span>
<span data-ttu-id="0ef99-121">Autentiseringsuppgifter, konto, klient organisation och abonnemang som används för kommunikation med Azure.</span><span class="sxs-lookup"><span data-stu-id="0ef99-121">The credentials, account, tenant, and subscription used for communication with azure.</span></span>
 
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

### <span data-ttu-id="0ef99-122">-Namn</span><span class="sxs-lookup"><span data-stu-id="0ef99-122">-Name</span></span>
<span data-ttu-id="0ef99-123">Anger ett eget namn på en leverantör.</span><span class="sxs-lookup"><span data-stu-id="0ef99-123">Specifies a friendly name of a provider.</span></span>
<span data-ttu-id="0ef99-124">Om du anger ett namn blir denna cmdlet den leverantören.</span><span class="sxs-lookup"><span data-stu-id="0ef99-124">If you specify a name, this cmdlet gets that provider.</span></span>

```yaml
Type: String
Parameter Sets: GetByName
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="0ef99-125">-OpenIdConnectProviderId</span><span class="sxs-lookup"><span data-stu-id="0ef99-125">-OpenIdConnectProviderId</span></span>
<span data-ttu-id="0ef99-126">Anger ett ID för den provider som denna cmdlet tar bort.</span><span class="sxs-lookup"><span data-stu-id="0ef99-126">Specifies an ID of the provider that this cmdlet removes.</span></span>
<span data-ttu-id="0ef99-127">Om du anger ett ID får denna cmdlet den leverantören.</span><span class="sxs-lookup"><span data-stu-id="0ef99-127">If you specify an ID, this cmdlet gets that provider.</span></span>

```yaml
Type: String
Parameter Sets: GetByOpenIdConnectProviderId
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="0ef99-128">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="0ef99-128">CommonParameters</span></span>
<span data-ttu-id="0ef99-129">Den här cmdleten har stöd för de gemensamma parametrarna:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-disvariable,-utbuffer,-PipelineVariable,-verbose,-WarningAction och-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="0ef99-129">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="0ef99-130">Mer information finns i about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="0ef99-130">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="0ef99-131">KOSTNADS</span><span class="sxs-lookup"><span data-stu-id="0ef99-131">INPUTS</span></span>

### <span data-ttu-id="0ef99-132">Ingen</span><span class="sxs-lookup"><span data-stu-id="0ef99-132">None</span></span>
<span data-ttu-id="0ef99-133">Denna cmdlet accepterar inte indata.</span><span class="sxs-lookup"><span data-stu-id="0ef99-133">This cmdlet does not accept any input.</span></span>

## <span data-ttu-id="0ef99-134">VÄRDEN</span><span class="sxs-lookup"><span data-stu-id="0ef99-134">OUTPUTS</span></span>

### <span data-ttu-id="0ef99-135">Microsoft. Azure. commands. ApiManagement. ServiceManagement. Models. PsApiManagementOpenIdConnectProvider</span><span class="sxs-lookup"><span data-stu-id="0ef99-135">Microsoft.Azure.Commands.ApiManagement.ServiceManagement.Models.PsApiManagementOpenIdConnectProvider</span></span>
<span data-ttu-id="0ef99-136">Detaljerna för OpenId som har kon figurer ATS i API Management Service.</span><span class="sxs-lookup"><span data-stu-id="0ef99-136">The detail of the OpenId connect Provider configured in API Management service.</span></span>

### <span data-ttu-id="0ef99-137">IList<Microsoft. Azure. commands. ApiManagement. ServiceManagement. Models. PsApiManagementOpenIdConnectProvider></span><span class="sxs-lookup"><span data-stu-id="0ef99-137">IList<Microsoft.Azure.Commands.ApiManagement.ServiceManagement.Models.PsApiManagementOpenIdConnectProvider></span></span>
<span data-ttu-id="0ef99-138">Listan med OpenId-partners som har kon figurer ATS i API Management Service.</span><span class="sxs-lookup"><span data-stu-id="0ef99-138">The list of OpenId Connect Providers configured in API Management service.</span></span>

## <span data-ttu-id="0ef99-139">ANMÄRKNINGAR</span><span class="sxs-lookup"><span data-stu-id="0ef99-139">NOTES</span></span>

## <span data-ttu-id="0ef99-140">RELATERADE LÄNKAR</span><span class="sxs-lookup"><span data-stu-id="0ef99-140">RELATED LINKS</span></span>

[<span data-ttu-id="0ef99-141">New-AzureRmApiManagementOpenIdConnectProvider</span><span class="sxs-lookup"><span data-stu-id="0ef99-141">New-AzureRmApiManagementOpenIdConnectProvider</span></span>](./New-AzureRmApiManagementOpenIdConnectProvider.md)

[<span data-ttu-id="0ef99-142">Remove-AzureRmApiManagementOpenIdConnectProvider</span><span class="sxs-lookup"><span data-stu-id="0ef99-142">Remove-AzureRmApiManagementOpenIdConnectProvider</span></span>](./Remove-AzureRmApiManagementOpenIdConnectProvider.md)

[<span data-ttu-id="0ef99-143">Set-AzureRmApiManagementOpenIdConnectProvider</span><span class="sxs-lookup"><span data-stu-id="0ef99-143">Set-AzureRmApiManagementOpenIdConnectProvider</span></span>](./Set-AzureRmApiManagementOpenIdConnectProvider.md)


