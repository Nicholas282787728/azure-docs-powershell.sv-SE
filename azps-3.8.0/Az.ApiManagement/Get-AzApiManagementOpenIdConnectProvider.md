---
external help file: Microsoft.Azure.PowerShell.Cmdlets.ApiManagement.ServiceManagement.dll-Help.xml
Module Name: Az.ApiManagement
ms.assetid: 15B6EAE2-56ED-4A01-B8EA-52B9FCDC1F66
online version: https://docs.microsoft.com/en-us/powershell/module/az.apimanagement/get-azapimanagementopenidconnectprovider
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/ApiManagement/ApiManagement/help/Get-AzApiManagementOpenIdConnectProvider.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/ApiManagement/ApiManagement/help/Get-AzApiManagementOpenIdConnectProvider.md
ms.openlocfilehash: b39ae66a5881acca72143274c479685ef1282854
ms.sourcegitcommit: 6a91b4c545350d316d3cf8c62f384478e3f3ba24
ms.translationtype: MT
ms.contentlocale: sv-SE
ms.lasthandoff: 04/21/2020
ms.locfileid: "94091603"
---
# <span data-ttu-id="e9fbd-101">Get-AzApiManagementOpenIdConnectProvider</span><span class="sxs-lookup"><span data-stu-id="e9fbd-101">Get-AzApiManagementOpenIdConnectProvider</span></span>

## <span data-ttu-id="e9fbd-102">Sammanfattning</span><span class="sxs-lookup"><span data-stu-id="e9fbd-102">SYNOPSIS</span></span>
<span data-ttu-id="e9fbd-103">Hämtar OpenID.</span><span class="sxs-lookup"><span data-stu-id="e9fbd-103">Gets OpenID Connect providers.</span></span>

## <span data-ttu-id="e9fbd-104">FRÅGESYNTAXEN</span><span class="sxs-lookup"><span data-stu-id="e9fbd-104">SYNTAX</span></span>

### <span data-ttu-id="e9fbd-105">GetAllOpenIdConnectProviders (standard)</span><span class="sxs-lookup"><span data-stu-id="e9fbd-105">GetAllOpenIdConnectProviders (Default)</span></span>
```
Get-AzApiManagementOpenIdConnectProvider -Context <PsApiManagementContext>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="e9fbd-106">GetByOpenIdConnectProviderId</span><span class="sxs-lookup"><span data-stu-id="e9fbd-106">GetByOpenIdConnectProviderId</span></span>
```
Get-AzApiManagementOpenIdConnectProvider -Context <PsApiManagementContext> [-OpenIdConnectProviderId <String>]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="e9fbd-107">GetByName</span><span class="sxs-lookup"><span data-stu-id="e9fbd-107">GetByName</span></span>
```
Get-AzApiManagementOpenIdConnectProvider -Context <PsApiManagementContext> [-Name <String>]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="e9fbd-108">PROBLEMBESKRIVNING</span><span class="sxs-lookup"><span data-stu-id="e9fbd-108">DESCRIPTION</span></span>
<span data-ttu-id="e9fbd-109">Cmdleten **Get-AzApiManagementOpenIdConnectProvider** hämtar OpenID Connect-leverantörer i Azure API Management.</span><span class="sxs-lookup"><span data-stu-id="e9fbd-109">The **Get-AzApiManagementOpenIdConnectProvider** cmdlet gets OpenID Connect providers in Azure API Management.</span></span>

## <span data-ttu-id="e9fbd-110">BESKRIVS</span><span class="sxs-lookup"><span data-stu-id="e9fbd-110">EXAMPLES</span></span>

### <span data-ttu-id="e9fbd-111">Exempel 1: Hämta alla leverantörer</span><span class="sxs-lookup"><span data-stu-id="e9fbd-111">Example 1: Get all providers</span></span>
```
PS C:\>$apimContext = New-AzApiManagementContext -ResourceGroupName "Api-Default-WestUS" -ServiceName "contoso"
PS C:\>Get-AzApiManagementOpenIdConnectProvider -Context $apimContext
```

<span data-ttu-id="e9fbd-112">Det här kommandot får alla OpenID Connect-leverantörer för angiven kontext.</span><span class="sxs-lookup"><span data-stu-id="e9fbd-112">This command gets all OpenID Connect providers for the specified context.</span></span>

### <span data-ttu-id="e9fbd-113">Exempel 2: skaffa en leverantör med hjälp av ett ID</span><span class="sxs-lookup"><span data-stu-id="e9fbd-113">Example 2: Get a provider by using an ID</span></span>
```
PS C:\>$apimContext = New-AzApiManagementContext -ResourceGroupName "Api-Default-WestUS" -ServiceName "contoso"
PS C:\>Get-AzApiManagementOpenIdConnectProvider -Context $apimContext -OpenIdConnectProviderId "OICProvider01"
```

<span data-ttu-id="e9fbd-114">Det här kommandot får leverantören med ID-OICProvider01.</span><span class="sxs-lookup"><span data-stu-id="e9fbd-114">This command gets the provider that has the ID OICProvider01.</span></span>

### <span data-ttu-id="e9fbd-115">Exempel 3: skaffa en leverantör genom att använda ett namn</span><span class="sxs-lookup"><span data-stu-id="e9fbd-115">Example 3: Get a provider by using a name</span></span>
```
PS C:\>$apimContext = New-AzApiManagementContext -ResourceGroupName "Api-Default-WestUS" -ServiceName "contoso"
PS C:\>Get-AzApiManagementOpenIdConnectProvider -Context $apimContext -Name "Contoso OpenID Connect Provider"
```

<span data-ttu-id="e9fbd-116">Med det här kommandot hämtas leverantören Contoso OpenID Connect-leverantör.</span><span class="sxs-lookup"><span data-stu-id="e9fbd-116">This command gets the provider named Contoso OpenID Connect Provider.</span></span>

## <span data-ttu-id="e9fbd-117">MALLPARAMETRAR</span><span class="sxs-lookup"><span data-stu-id="e9fbd-117">PARAMETERS</span></span>

### <span data-ttu-id="e9fbd-118">-Kontext</span><span class="sxs-lookup"><span data-stu-id="e9fbd-118">-Context</span></span>
<span data-ttu-id="e9fbd-119">Anger ett **PsApiManagementContext** -objekt.</span><span class="sxs-lookup"><span data-stu-id="e9fbd-119">Specifies a **PsApiManagementContext** object.</span></span>

```yaml
Type: Microsoft.Azure.Commands.ApiManagement.ServiceManagement.Models.PsApiManagementContext
Parameter Sets: (All)
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName, ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="e9fbd-120">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="e9fbd-120">-DefaultProfile</span></span>
<span data-ttu-id="e9fbd-121">Autentiseringsuppgifter, konto, klient organisation och abonnemang som används för kommunikation med Azure.</span><span class="sxs-lookup"><span data-stu-id="e9fbd-121">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="e9fbd-122">-Namn</span><span class="sxs-lookup"><span data-stu-id="e9fbd-122">-Name</span></span>
<span data-ttu-id="e9fbd-123">Anger ett eget namn på en leverantör.</span><span class="sxs-lookup"><span data-stu-id="e9fbd-123">Specifies a friendly name of a provider.</span></span>
<span data-ttu-id="e9fbd-124">Om du anger ett namn blir denna cmdlet den leverantören.</span><span class="sxs-lookup"><span data-stu-id="e9fbd-124">If you specify a name, this cmdlet gets that provider.</span></span>

```yaml
Type: System.String
Parameter Sets: GetByName
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="e9fbd-125">-OpenIdConnectProviderId</span><span class="sxs-lookup"><span data-stu-id="e9fbd-125">-OpenIdConnectProviderId</span></span>
<span data-ttu-id="e9fbd-126">Anger ett ID för den provider som denna cmdlet tar bort.</span><span class="sxs-lookup"><span data-stu-id="e9fbd-126">Specifies an ID of the provider that this cmdlet removes.</span></span>
<span data-ttu-id="e9fbd-127">Om du anger ett ID får denna cmdlet den leverantören.</span><span class="sxs-lookup"><span data-stu-id="e9fbd-127">If you specify an ID, this cmdlet gets that provider.</span></span>

```yaml
Type: System.String
Parameter Sets: GetByOpenIdConnectProviderId
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="e9fbd-128">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="e9fbd-128">CommonParameters</span></span>
<span data-ttu-id="e9fbd-129">Den här cmdleten har stöd för de gemensamma parametrarna:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-disvariable,-utbuffer,-PipelineVariable,-verbose,-WarningAction och-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="e9fbd-129">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="e9fbd-130">Mer information finns i [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="e9fbd-130">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="e9fbd-131">KOSTNADS</span><span class="sxs-lookup"><span data-stu-id="e9fbd-131">INPUTS</span></span>

### <span data-ttu-id="e9fbd-132">Microsoft. Azure. commands. ApiManagement. ServiceManagement. Models. PsApiManagementContext</span><span class="sxs-lookup"><span data-stu-id="e9fbd-132">Microsoft.Azure.Commands.ApiManagement.ServiceManagement.Models.PsApiManagementContext</span></span>

### <span data-ttu-id="e9fbd-133">System. String</span><span class="sxs-lookup"><span data-stu-id="e9fbd-133">System.String</span></span>

## <span data-ttu-id="e9fbd-134">VÄRDEN</span><span class="sxs-lookup"><span data-stu-id="e9fbd-134">OUTPUTS</span></span>

### <span data-ttu-id="e9fbd-135">Microsoft. Azure. commands. ApiManagement. ServiceManagement. Models. PsApiManagementOpenIdConnectProvider</span><span class="sxs-lookup"><span data-stu-id="e9fbd-135">Microsoft.Azure.Commands.ApiManagement.ServiceManagement.Models.PsApiManagementOpenIdConnectProvider</span></span>

## <span data-ttu-id="e9fbd-136">ANMÄRKNINGAR</span><span class="sxs-lookup"><span data-stu-id="e9fbd-136">NOTES</span></span>

## <span data-ttu-id="e9fbd-137">RELATERADE LÄNKAR</span><span class="sxs-lookup"><span data-stu-id="e9fbd-137">RELATED LINKS</span></span>

[<span data-ttu-id="e9fbd-138">New-AzApiManagementOpenIdConnectProvider</span><span class="sxs-lookup"><span data-stu-id="e9fbd-138">New-AzApiManagementOpenIdConnectProvider</span></span>](./New-AzApiManagementOpenIdConnectProvider.md)

[<span data-ttu-id="e9fbd-139">Remove-AzApiManagementOpenIdConnectProvider</span><span class="sxs-lookup"><span data-stu-id="e9fbd-139">Remove-AzApiManagementOpenIdConnectProvider</span></span>](./Remove-AzApiManagementOpenIdConnectProvider.md)

[<span data-ttu-id="e9fbd-140">Set-AzApiManagementOpenIdConnectProvider</span><span class="sxs-lookup"><span data-stu-id="e9fbd-140">Set-AzApiManagementOpenIdConnectProvider</span></span>](./Set-AzApiManagementOpenIdConnectProvider.md)


