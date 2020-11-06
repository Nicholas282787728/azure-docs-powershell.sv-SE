---
external help file: Microsoft.Azure.Commands.ApiManagement.ServiceManagement.dll-Help.xml
ms.assetid: D5B18FF4-3294-4561-A4CD-CF0FA5E4A59B
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.apimanagement/new-azurermapimanagementopenidconnectprovider
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/ApiManagement/Commands.ApiManagement/help/New-AzureRmApiManagementOpenIdConnectProvider.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/ApiManagement/Commands.ApiManagement/help/New-AzureRmApiManagementOpenIdConnectProvider.md
ms.openlocfilehash: 088b88bcaa7f0d493552060c150e9d76a4b16c7f
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: sv-SE
ms.lasthandoff: 08/20/2020
ms.locfileid: "93573582"
---
# <span data-ttu-id="fd24a-101">New-AzureRmApiManagementOpenIdConnectProvider</span><span class="sxs-lookup"><span data-stu-id="fd24a-101">New-AzureRmApiManagementOpenIdConnectProvider</span></span>

## <span data-ttu-id="fd24a-102">Sammanfattning</span><span class="sxs-lookup"><span data-stu-id="fd24a-102">SYNOPSIS</span></span>
<span data-ttu-id="fd24a-103">Skapar en OpenID.</span><span class="sxs-lookup"><span data-stu-id="fd24a-103">Creates an OpenID Connect provider.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="fd24a-104">FRÅGESYNTAXEN</span><span class="sxs-lookup"><span data-stu-id="fd24a-104">SYNTAX</span></span>

```
New-AzureRmApiManagementOpenIdConnectProvider -Context <PsApiManagementContext>
 [-OpenIdConnectProviderId <String>] -Name <String> -MetadataEndpointUri <String> -ClientId <String>
 [-ClientSecret <String>] [-Description <String>] [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

## <span data-ttu-id="fd24a-105">PROBLEMBESKRIVNING</span><span class="sxs-lookup"><span data-stu-id="fd24a-105">DESCRIPTION</span></span>
<span data-ttu-id="fd24a-106">Cmdleten **New-AzureRmApiManagementOpenIdConnectProvider** skapar en OpenID Connect-leverantör i Azure API Management.</span><span class="sxs-lookup"><span data-stu-id="fd24a-106">The **New-AzureRmApiManagementOpenIdConnectProvider** cmdlet creates an OpenID Connect provider in Azure API Management.</span></span>

## <span data-ttu-id="fd24a-107">BESKRIVS</span><span class="sxs-lookup"><span data-stu-id="fd24a-107">EXAMPLES</span></span>

### <span data-ttu-id="fd24a-108">Exempel 1: skapa en leverantör</span><span class="sxs-lookup"><span data-stu-id="fd24a-108">Example 1: Create a provider</span></span>
```
PS C:\>$apimContext = New-AzureRmApiManagementContext -ResourceGroupName "Api-Default-WestUS" -ServiceName "contoso"
PS C:\>New-AzureRmApiManagementOpenIdConnectProvider -Context $apimContext -OpenIdConnectProviderId "OICProvicer01" -Name "Contoso OpenID Connect Provider" -MetadataEndpointUri "https://openid.provider/configuration" -ClientId "12432143" -Description "OpenID Connect provider description"
```

<span data-ttu-id="fd24a-109">Det här kommandot skapar en OpenID Connect- **leverantör** som heter Contoso OpenID Connect-leverantören</span><span class="sxs-lookup"><span data-stu-id="fd24a-109">This command creates an OpenID Connect **Provider** named Contoso OpenID Connect Provider</span></span>

## <span data-ttu-id="fd24a-110">MALLPARAMETRAR</span><span class="sxs-lookup"><span data-stu-id="fd24a-110">PARAMETERS</span></span>

### <span data-ttu-id="fd24a-111">-ClientId</span><span class="sxs-lookup"><span data-stu-id="fd24a-111">-ClientId</span></span>
<span data-ttu-id="fd24a-112">Anger klient-ID för Developer Console.</span><span class="sxs-lookup"><span data-stu-id="fd24a-112">Specifies the client ID of the developer console.</span></span>

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

### <span data-ttu-id="fd24a-113">-ClientSecret</span><span class="sxs-lookup"><span data-stu-id="fd24a-113">-ClientSecret</span></span>
<span data-ttu-id="fd24a-114">Anger utvecklarens klient hemlighet.</span><span class="sxs-lookup"><span data-stu-id="fd24a-114">Specifies the client secret of the developer console.</span></span>

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

### <span data-ttu-id="fd24a-115">-Kontext</span><span class="sxs-lookup"><span data-stu-id="fd24a-115">-Context</span></span>
<span data-ttu-id="fd24a-116">Anger ett **PsApiManagementContext** -objekt.</span><span class="sxs-lookup"><span data-stu-id="fd24a-116">Specifies a **PsApiManagementContext** object.</span></span>

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

### <span data-ttu-id="fd24a-117">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="fd24a-117">-DefaultProfile</span></span>
<span data-ttu-id="fd24a-118">Autentiseringsuppgifter, konto, klient organisation och abonnemang som används för kommunikation med Azure.</span><span class="sxs-lookup"><span data-stu-id="fd24a-118">The credentials, account, tenant, and subscription used for communication with azure.</span></span>
 
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

### <span data-ttu-id="fd24a-119">-Beskrivning</span><span class="sxs-lookup"><span data-stu-id="fd24a-119">-Description</span></span>
<span data-ttu-id="fd24a-120">Anger en beskrivning.</span><span class="sxs-lookup"><span data-stu-id="fd24a-120">Specifies a description.</span></span>

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

### <span data-ttu-id="fd24a-121">-MetadataEndpointUri</span><span class="sxs-lookup"><span data-stu-id="fd24a-121">-MetadataEndpointUri</span></span>
<span data-ttu-id="fd24a-122">Anger en URI för metadata-slutpunkt för providern.</span><span class="sxs-lookup"><span data-stu-id="fd24a-122">Specifies a metadata endpoint URI of the provider.</span></span>

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

### <span data-ttu-id="fd24a-123">-Namn</span><span class="sxs-lookup"><span data-stu-id="fd24a-123">-Name</span></span>
<span data-ttu-id="fd24a-124">Anger ett eget namn för leverantören.</span><span class="sxs-lookup"><span data-stu-id="fd24a-124">Specifies a friendly name for the provider.</span></span>

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

### <span data-ttu-id="fd24a-125">-OpenIdConnectProviderId</span><span class="sxs-lookup"><span data-stu-id="fd24a-125">-OpenIdConnectProviderId</span></span>
<span data-ttu-id="fd24a-126">Anger ett ID för leverantören.</span><span class="sxs-lookup"><span data-stu-id="fd24a-126">Specifies an ID for the provider.</span></span>
<span data-ttu-id="fd24a-127">Om du inte anger något ID skapar den här cmdleten en.</span><span class="sxs-lookup"><span data-stu-id="fd24a-127">If you do not specify an ID, this cmdlet generates one.</span></span>

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

### <span data-ttu-id="fd24a-128">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="fd24a-128">CommonParameters</span></span>
<span data-ttu-id="fd24a-129">Den här cmdleten har stöd för de gemensamma parametrarna:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-disvariable,-utbuffer,-PipelineVariable,-verbose,-WarningAction och-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="fd24a-129">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="fd24a-130">Mer information finns i about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="fd24a-130">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="fd24a-131">KOSTNADS</span><span class="sxs-lookup"><span data-stu-id="fd24a-131">INPUTS</span></span>

### <span data-ttu-id="fd24a-132">Ingen</span><span class="sxs-lookup"><span data-stu-id="fd24a-132">None</span></span>
<span data-ttu-id="fd24a-133">Denna cmdlet accepterar inte indata.</span><span class="sxs-lookup"><span data-stu-id="fd24a-133">This cmdlet does not accept any input.</span></span>

## <span data-ttu-id="fd24a-134">VÄRDEN</span><span class="sxs-lookup"><span data-stu-id="fd24a-134">OUTPUTS</span></span>

### <span data-ttu-id="fd24a-135">Microsoft. Azure. commands. ApiManagement. ServiceManagement. Models. PsApiManagementOpenIdConnectProvider</span><span class="sxs-lookup"><span data-stu-id="fd24a-135">Microsoft.Azure.Commands.ApiManagement.ServiceManagement.Models.PsApiManagementOpenIdConnectProvider</span></span>

## <span data-ttu-id="fd24a-136">ANMÄRKNINGAR</span><span class="sxs-lookup"><span data-stu-id="fd24a-136">NOTES</span></span>

## <span data-ttu-id="fd24a-137">RELATERADE LÄNKAR</span><span class="sxs-lookup"><span data-stu-id="fd24a-137">RELATED LINKS</span></span>

[<span data-ttu-id="fd24a-138">Get-AzureRmApiManagementOpenIdConnectProvider</span><span class="sxs-lookup"><span data-stu-id="fd24a-138">Get-AzureRmApiManagementOpenIdConnectProvider</span></span>](./Get-AzureRmApiManagementOpenIdConnectProvider.md)

[<span data-ttu-id="fd24a-139">Remove-AzureRmApiManagementOpenIdConnectProvider</span><span class="sxs-lookup"><span data-stu-id="fd24a-139">Remove-AzureRmApiManagementOpenIdConnectProvider</span></span>](./Remove-AzureRmApiManagementOpenIdConnectProvider.md)

[<span data-ttu-id="fd24a-140">Set-AzureRmApiManagementOpenIdConnectProvider</span><span class="sxs-lookup"><span data-stu-id="fd24a-140">Set-AzureRmApiManagementOpenIdConnectProvider</span></span>](./Set-AzureRmApiManagementOpenIdConnectProvider.md)


