---
external help file: Microsoft.Azure.PowerShell.Cmdlets.ApiManagement.ServiceManagement.dll-Help.xml
Module Name: Az.ApiManagement
ms.assetid: D5B18FF4-3294-4561-A4CD-CF0FA5E4A59B
online version: https://docs.microsoft.com/en-us/powershell/module/az.apimanagement/new-azapimanagementopenidconnectprovider
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/ApiManagement/ApiManagement/help/New-AzApiManagementOpenIdConnectProvider.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/ApiManagement/ApiManagement/help/New-AzApiManagementOpenIdConnectProvider.md
ms.openlocfilehash: 3b4cec203e39401885874db5391f62a9f1663342
ms.sourcegitcommit: 4d2c178cd6df9151877b08d54c1f4a228dbec9d1
ms.translationtype: MT
ms.contentlocale: sv-SE
ms.lasthandoff: 01/29/2020
ms.locfileid: "93917853"
---
# <span data-ttu-id="ad4c2-101">New-AzApiManagementOpenIdConnectProvider</span><span class="sxs-lookup"><span data-stu-id="ad4c2-101">New-AzApiManagementOpenIdConnectProvider</span></span>

## <span data-ttu-id="ad4c2-102">Sammanfattning</span><span class="sxs-lookup"><span data-stu-id="ad4c2-102">SYNOPSIS</span></span>
<span data-ttu-id="ad4c2-103">Skapar en OpenID.</span><span class="sxs-lookup"><span data-stu-id="ad4c2-103">Creates an OpenID Connect provider.</span></span>

## <span data-ttu-id="ad4c2-104">FRÅGESYNTAXEN</span><span class="sxs-lookup"><span data-stu-id="ad4c2-104">SYNTAX</span></span>

```
New-AzApiManagementOpenIdConnectProvider -Context <PsApiManagementContext> [-OpenIdConnectProviderId <String>]
 -Name <String> -MetadataEndpointUri <String> -ClientId <String> [-ClientSecret <String>]
 [-Description <String>] [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="ad4c2-105">PROBLEMBESKRIVNING</span><span class="sxs-lookup"><span data-stu-id="ad4c2-105">DESCRIPTION</span></span>
<span data-ttu-id="ad4c2-106">Cmdleten **New-AzApiManagementOpenIdConnectProvider** skapar en OpenID Connect-leverantör i Azure API Management.</span><span class="sxs-lookup"><span data-stu-id="ad4c2-106">The **New-AzApiManagementOpenIdConnectProvider** cmdlet creates an OpenID Connect provider in Azure API Management.</span></span>

## <span data-ttu-id="ad4c2-107">BESKRIVS</span><span class="sxs-lookup"><span data-stu-id="ad4c2-107">EXAMPLES</span></span>

### <span data-ttu-id="ad4c2-108">Exempel 1: skapa en leverantör</span><span class="sxs-lookup"><span data-stu-id="ad4c2-108">Example 1: Create a provider</span></span>
```
PS C:\>$apimContext = New-AzApiManagementContext -ResourceGroupName "Api-Default-WestUS" -ServiceName "contoso"
PS C:\>New-AzApiManagementOpenIdConnectProvider -Context $apimContext -OpenIdConnectProviderId "OICProvicer01" -Name "Contoso OpenID Connect Provider" -MetadataEndpointUri "https://openid.provider/configuration" -ClientId "12432143" -Description "OpenID Connect provider description"
```

<span data-ttu-id="ad4c2-109">Det här kommandot skapar en OpenID Connect- **leverantör** som heter Contoso OpenID Connect-leverantören</span><span class="sxs-lookup"><span data-stu-id="ad4c2-109">This command creates an OpenID Connect **Provider** named Contoso OpenID Connect Provider</span></span>

## <span data-ttu-id="ad4c2-110">MALLPARAMETRAR</span><span class="sxs-lookup"><span data-stu-id="ad4c2-110">PARAMETERS</span></span>

### <span data-ttu-id="ad4c2-111">-ClientId</span><span class="sxs-lookup"><span data-stu-id="ad4c2-111">-ClientId</span></span>
<span data-ttu-id="ad4c2-112">Anger klient-ID för Developer Console.</span><span class="sxs-lookup"><span data-stu-id="ad4c2-112">Specifies the client ID of the developer console.</span></span>

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

### <span data-ttu-id="ad4c2-113">-ClientSecret</span><span class="sxs-lookup"><span data-stu-id="ad4c2-113">-ClientSecret</span></span>
<span data-ttu-id="ad4c2-114">Anger utvecklarens klient hemlighet.</span><span class="sxs-lookup"><span data-stu-id="ad4c2-114">Specifies the client secret of the developer console.</span></span>

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

### <span data-ttu-id="ad4c2-115">-Kontext</span><span class="sxs-lookup"><span data-stu-id="ad4c2-115">-Context</span></span>
<span data-ttu-id="ad4c2-116">Anger ett **PsApiManagementContext** -objekt.</span><span class="sxs-lookup"><span data-stu-id="ad4c2-116">Specifies a **PsApiManagementContext** object.</span></span>

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

### <span data-ttu-id="ad4c2-117">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="ad4c2-117">-DefaultProfile</span></span>
<span data-ttu-id="ad4c2-118">Autentiseringsuppgifter, konto, klient organisation och abonnemang som används för kommunikation med Azure.</span><span class="sxs-lookup"><span data-stu-id="ad4c2-118">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="ad4c2-119">-Beskrivning</span><span class="sxs-lookup"><span data-stu-id="ad4c2-119">-Description</span></span>
<span data-ttu-id="ad4c2-120">Anger en beskrivning.</span><span class="sxs-lookup"><span data-stu-id="ad4c2-120">Specifies a description.</span></span>

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

### <span data-ttu-id="ad4c2-121">-MetadataEndpointUri</span><span class="sxs-lookup"><span data-stu-id="ad4c2-121">-MetadataEndpointUri</span></span>
<span data-ttu-id="ad4c2-122">Anger en URI för metadata-slutpunkt för providern.</span><span class="sxs-lookup"><span data-stu-id="ad4c2-122">Specifies a metadata endpoint URI of the provider.</span></span>

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

### <span data-ttu-id="ad4c2-123">-Namn</span><span class="sxs-lookup"><span data-stu-id="ad4c2-123">-Name</span></span>
<span data-ttu-id="ad4c2-124">Anger ett eget namn för leverantören.</span><span class="sxs-lookup"><span data-stu-id="ad4c2-124">Specifies a friendly name for the provider.</span></span>

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

### <span data-ttu-id="ad4c2-125">-OpenIdConnectProviderId</span><span class="sxs-lookup"><span data-stu-id="ad4c2-125">-OpenIdConnectProviderId</span></span>
<span data-ttu-id="ad4c2-126">Anger ett ID för leverantören.</span><span class="sxs-lookup"><span data-stu-id="ad4c2-126">Specifies an ID for the provider.</span></span>
<span data-ttu-id="ad4c2-127">Om du inte anger något ID skapar den här cmdleten en.</span><span class="sxs-lookup"><span data-stu-id="ad4c2-127">If you do not specify an ID, this cmdlet generates one.</span></span>

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

### <span data-ttu-id="ad4c2-128">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="ad4c2-128">CommonParameters</span></span>
<span data-ttu-id="ad4c2-129">Den här cmdleten har stöd för de gemensamma parametrarna:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-disvariable,-utbuffer,-PipelineVariable,-verbose,-WarningAction och-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="ad4c2-129">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="ad4c2-130">Mer information finns i about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="ad4c2-130">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="ad4c2-131">KOSTNADS</span><span class="sxs-lookup"><span data-stu-id="ad4c2-131">INPUTS</span></span>

### <span data-ttu-id="ad4c2-132">Microsoft. Azure. commands. ApiManagement. ServiceManagement. Models. PsApiManagementContext</span><span class="sxs-lookup"><span data-stu-id="ad4c2-132">Microsoft.Azure.Commands.ApiManagement.ServiceManagement.Models.PsApiManagementContext</span></span>

### <span data-ttu-id="ad4c2-133">System. String</span><span class="sxs-lookup"><span data-stu-id="ad4c2-133">System.String</span></span>

## <span data-ttu-id="ad4c2-134">VÄRDEN</span><span class="sxs-lookup"><span data-stu-id="ad4c2-134">OUTPUTS</span></span>

### <span data-ttu-id="ad4c2-135">Microsoft. Azure. commands. ApiManagement. ServiceManagement. Models. PsApiManagementOpenIdConnectProvider</span><span class="sxs-lookup"><span data-stu-id="ad4c2-135">Microsoft.Azure.Commands.ApiManagement.ServiceManagement.Models.PsApiManagementOpenIdConnectProvider</span></span>

## <span data-ttu-id="ad4c2-136">ANMÄRKNINGAR</span><span class="sxs-lookup"><span data-stu-id="ad4c2-136">NOTES</span></span>

## <span data-ttu-id="ad4c2-137">RELATERADE LÄNKAR</span><span class="sxs-lookup"><span data-stu-id="ad4c2-137">RELATED LINKS</span></span>

[<span data-ttu-id="ad4c2-138">Get-AzApiManagementOpenIdConnectProvider</span><span class="sxs-lookup"><span data-stu-id="ad4c2-138">Get-AzApiManagementOpenIdConnectProvider</span></span>](./Get-AzApiManagementOpenIdConnectProvider.md)

[<span data-ttu-id="ad4c2-139">Remove-AzApiManagementOpenIdConnectProvider</span><span class="sxs-lookup"><span data-stu-id="ad4c2-139">Remove-AzApiManagementOpenIdConnectProvider</span></span>](./Remove-AzApiManagementOpenIdConnectProvider.md)

[<span data-ttu-id="ad4c2-140">Set-AzApiManagementOpenIdConnectProvider</span><span class="sxs-lookup"><span data-stu-id="ad4c2-140">Set-AzApiManagementOpenIdConnectProvider</span></span>](./Set-AzApiManagementOpenIdConnectProvider.md)


