---
external help file: Microsoft.Azure.Commands.ApiManagement.ServiceManagement.dll-Help.xml
Module Name: AzureRM.ApiManagement
ms.assetid: D5B18FF4-3294-4561-A4CD-CF0FA5E4A59B
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.apimanagement/new-azurermapimanagementopenidconnectprovider
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/ApiManagement/Commands.ApiManagement/help/New-AzureRmApiManagementOpenIdConnectProvider.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/ApiManagement/Commands.ApiManagement/help/New-AzureRmApiManagementOpenIdConnectProvider.md
ms.openlocfilehash: c338cd8b2ea3ce2a464a7975ecac959bc1e52140
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: sv-SE
ms.lasthandoff: 08/20/2020
ms.locfileid: "93756422"
---
# <span data-ttu-id="47823-101">New-AzureRmApiManagementOpenIdConnectProvider</span><span class="sxs-lookup"><span data-stu-id="47823-101">New-AzureRmApiManagementOpenIdConnectProvider</span></span>

## <span data-ttu-id="47823-102">Sammanfattning</span><span class="sxs-lookup"><span data-stu-id="47823-102">SYNOPSIS</span></span>
<span data-ttu-id="47823-103">Skapar en OpenID.</span><span class="sxs-lookup"><span data-stu-id="47823-103">Creates an OpenID Connect provider.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="47823-104">FRÅGESYNTAXEN</span><span class="sxs-lookup"><span data-stu-id="47823-104">SYNTAX</span></span>

```
New-AzureRmApiManagementOpenIdConnectProvider -Context <PsApiManagementContext>
 [-OpenIdConnectProviderId <String>] -Name <String> -MetadataEndpointUri <String> -ClientId <String>
 [-ClientSecret <String>] [-Description <String>] [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

## <span data-ttu-id="47823-105">PROBLEMBESKRIVNING</span><span class="sxs-lookup"><span data-stu-id="47823-105">DESCRIPTION</span></span>
<span data-ttu-id="47823-106">Cmdleten **New-AzureRmApiManagementOpenIdConnectProvider** skapar en OpenID Connect-leverantör i Azure API Management.</span><span class="sxs-lookup"><span data-stu-id="47823-106">The **New-AzureRmApiManagementOpenIdConnectProvider** cmdlet creates an OpenID Connect provider in Azure API Management.</span></span>

## <span data-ttu-id="47823-107">BESKRIVS</span><span class="sxs-lookup"><span data-stu-id="47823-107">EXAMPLES</span></span>

### <span data-ttu-id="47823-108">Exempel 1: skapa en leverantör</span><span class="sxs-lookup"><span data-stu-id="47823-108">Example 1: Create a provider</span></span>
```
PS C:\>$apimContext = New-AzureRmApiManagementContext -ResourceGroupName "Api-Default-WestUS" -ServiceName "contoso"
PS C:\>New-AzureRmApiManagementOpenIdConnectProvider -Context $apimContext -OpenIdConnectProviderId "OICProvicer01" -Name "Contoso OpenID Connect Provider" -MetadataEndpointUri "https://openid.provider/configuration" -ClientId "12432143" -Description "OpenID Connect provider description"
```

<span data-ttu-id="47823-109">Det här kommandot skapar en OpenID Connect- **leverantör** som heter Contoso OpenID Connect-leverantören</span><span class="sxs-lookup"><span data-stu-id="47823-109">This command creates an OpenID Connect **Provider** named Contoso OpenID Connect Provider</span></span>

## <span data-ttu-id="47823-110">MALLPARAMETRAR</span><span class="sxs-lookup"><span data-stu-id="47823-110">PARAMETERS</span></span>

### <span data-ttu-id="47823-111">-ClientId</span><span class="sxs-lookup"><span data-stu-id="47823-111">-ClientId</span></span>
<span data-ttu-id="47823-112">Anger klient-ID för Developer Console.</span><span class="sxs-lookup"><span data-stu-id="47823-112">Specifies the client ID of the developer console.</span></span>

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

### <span data-ttu-id="47823-113">-ClientSecret</span><span class="sxs-lookup"><span data-stu-id="47823-113">-ClientSecret</span></span>
<span data-ttu-id="47823-114">Anger utvecklarens klient hemlighet.</span><span class="sxs-lookup"><span data-stu-id="47823-114">Specifies the client secret of the developer console.</span></span>

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

### <span data-ttu-id="47823-115">-Kontext</span><span class="sxs-lookup"><span data-stu-id="47823-115">-Context</span></span>
<span data-ttu-id="47823-116">Anger ett **PsApiManagementContext** -objekt.</span><span class="sxs-lookup"><span data-stu-id="47823-116">Specifies a **PsApiManagementContext** object.</span></span>

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

### <span data-ttu-id="47823-117">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="47823-117">-DefaultProfile</span></span>
<span data-ttu-id="47823-118">Autentiseringsuppgifter, konto, klient organisation och abonnemang som används för kommunikation med Azure.</span><span class="sxs-lookup"><span data-stu-id="47823-118">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="47823-119">-Beskrivning</span><span class="sxs-lookup"><span data-stu-id="47823-119">-Description</span></span>
<span data-ttu-id="47823-120">Anger en beskrivning.</span><span class="sxs-lookup"><span data-stu-id="47823-120">Specifies a description.</span></span>

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

### <span data-ttu-id="47823-121">-MetadataEndpointUri</span><span class="sxs-lookup"><span data-stu-id="47823-121">-MetadataEndpointUri</span></span>
<span data-ttu-id="47823-122">Anger en URI för metadata-slutpunkt för providern.</span><span class="sxs-lookup"><span data-stu-id="47823-122">Specifies a metadata endpoint URI of the provider.</span></span>

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

### <span data-ttu-id="47823-123">-Namn</span><span class="sxs-lookup"><span data-stu-id="47823-123">-Name</span></span>
<span data-ttu-id="47823-124">Anger ett eget namn för leverantören.</span><span class="sxs-lookup"><span data-stu-id="47823-124">Specifies a friendly name for the provider.</span></span>

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

### <span data-ttu-id="47823-125">-OpenIdConnectProviderId</span><span class="sxs-lookup"><span data-stu-id="47823-125">-OpenIdConnectProviderId</span></span>
<span data-ttu-id="47823-126">Anger ett ID för leverantören.</span><span class="sxs-lookup"><span data-stu-id="47823-126">Specifies an ID for the provider.</span></span>
<span data-ttu-id="47823-127">Om du inte anger något ID skapar den här cmdleten en.</span><span class="sxs-lookup"><span data-stu-id="47823-127">If you do not specify an ID, this cmdlet generates one.</span></span>

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

### <span data-ttu-id="47823-128">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="47823-128">CommonParameters</span></span>
<span data-ttu-id="47823-129">Den här cmdleten har stöd för de gemensamma parametrarna:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-disvariable,-utbuffer,-PipelineVariable,-verbose,-WarningAction och-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="47823-129">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="47823-130">Mer information finns i about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="47823-130">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="47823-131">KOSTNADS</span><span class="sxs-lookup"><span data-stu-id="47823-131">INPUTS</span></span>

### <span data-ttu-id="47823-132">Microsoft. Azure. commands. ApiManagement. ServiceManagement. Models. PsApiManagementContext</span><span class="sxs-lookup"><span data-stu-id="47823-132">Microsoft.Azure.Commands.ApiManagement.ServiceManagement.Models.PsApiManagementContext</span></span>

### <span data-ttu-id="47823-133">System. String</span><span class="sxs-lookup"><span data-stu-id="47823-133">System.String</span></span>

## <span data-ttu-id="47823-134">VÄRDEN</span><span class="sxs-lookup"><span data-stu-id="47823-134">OUTPUTS</span></span>

### <span data-ttu-id="47823-135">Microsoft. Azure. commands. ApiManagement. ServiceManagement. Models. PsApiManagementOpenIdConnectProvider</span><span class="sxs-lookup"><span data-stu-id="47823-135">Microsoft.Azure.Commands.ApiManagement.ServiceManagement.Models.PsApiManagementOpenIdConnectProvider</span></span>

## <span data-ttu-id="47823-136">ANMÄRKNINGAR</span><span class="sxs-lookup"><span data-stu-id="47823-136">NOTES</span></span>

## <span data-ttu-id="47823-137">RELATERADE LÄNKAR</span><span class="sxs-lookup"><span data-stu-id="47823-137">RELATED LINKS</span></span>

[<span data-ttu-id="47823-138">Get-AzureRmApiManagementOpenIdConnectProvider</span><span class="sxs-lookup"><span data-stu-id="47823-138">Get-AzureRmApiManagementOpenIdConnectProvider</span></span>](./Get-AzureRmApiManagementOpenIdConnectProvider.md)

[<span data-ttu-id="47823-139">Remove-AzureRmApiManagementOpenIdConnectProvider</span><span class="sxs-lookup"><span data-stu-id="47823-139">Remove-AzureRmApiManagementOpenIdConnectProvider</span></span>](./Remove-AzureRmApiManagementOpenIdConnectProvider.md)

[<span data-ttu-id="47823-140">Set-AzureRmApiManagementOpenIdConnectProvider</span><span class="sxs-lookup"><span data-stu-id="47823-140">Set-AzureRmApiManagementOpenIdConnectProvider</span></span>](./Set-AzureRmApiManagementOpenIdConnectProvider.md)


