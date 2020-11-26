---
external help file: Microsoft.Azure.PowerShell.Cmdlets.ApiManagement.ServiceManagement.dll-Help.xml
Module Name: Az.ApiManagement
ms.assetid: 15B6EAE2-56ED-4A01-B8EA-52B9FCDC1F66
online version: https://docs.microsoft.com/en-us/powershell/module/az.apimanagement/get-azapimanagementopenidconnectprovider
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/ApiManagement/ApiManagement/help/Get-AzApiManagementOpenIdConnectProvider.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/ApiManagement/ApiManagement/help/Get-AzApiManagementOpenIdConnectProvider.md
ms.openlocfilehash: 6968b4ea1b222d0f046611f10e65f8073a4ba86a
ms.sourcegitcommit: b4a38bcb0501a9016a4998efd377aa75d3ef9ce8
ms.translationtype: MT
ms.contentlocale: sv-SE
ms.lasthandoff: 10/27/2020
ms.locfileid: "94326051"
---
# <span data-ttu-id="2a656-101">Get-AzApiManagementOpenIdConnectProvider</span><span class="sxs-lookup"><span data-stu-id="2a656-101">Get-AzApiManagementOpenIdConnectProvider</span></span>

## <span data-ttu-id="2a656-102">Sammanfattning</span><span class="sxs-lookup"><span data-stu-id="2a656-102">SYNOPSIS</span></span>
<span data-ttu-id="2a656-103">Hämtar OpenID.</span><span class="sxs-lookup"><span data-stu-id="2a656-103">Gets OpenID Connect providers.</span></span>

## <span data-ttu-id="2a656-104">FRÅGESYNTAXEN</span><span class="sxs-lookup"><span data-stu-id="2a656-104">SYNTAX</span></span>

### <span data-ttu-id="2a656-105">GetAllOpenIdConnectProviders (standard)</span><span class="sxs-lookup"><span data-stu-id="2a656-105">GetAllOpenIdConnectProviders (Default)</span></span>
```
Get-AzApiManagementOpenIdConnectProvider -Context <PsApiManagementContext>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="2a656-106">GetByOpenIdConnectProviderId</span><span class="sxs-lookup"><span data-stu-id="2a656-106">GetByOpenIdConnectProviderId</span></span>
```
Get-AzApiManagementOpenIdConnectProvider -Context <PsApiManagementContext> [-OpenIdConnectProviderId <String>]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="2a656-107">GetByName</span><span class="sxs-lookup"><span data-stu-id="2a656-107">GetByName</span></span>
```
Get-AzApiManagementOpenIdConnectProvider -Context <PsApiManagementContext> [-Name <String>]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="2a656-108">PROBLEMBESKRIVNING</span><span class="sxs-lookup"><span data-stu-id="2a656-108">DESCRIPTION</span></span>
<span data-ttu-id="2a656-109">Cmdleten **Get-AzApiManagementOpenIdConnectProvider** hämtar OpenID Connect-leverantörer i Azure API Management.</span><span class="sxs-lookup"><span data-stu-id="2a656-109">The **Get-AzApiManagementOpenIdConnectProvider** cmdlet gets OpenID Connect providers in Azure API Management.</span></span>
<span data-ttu-id="2a656-110">ClientSecret tas inte med i resultatet.</span><span class="sxs-lookup"><span data-stu-id="2a656-110">ClientSecret will not be included into result details.</span></span> <span data-ttu-id="2a656-111">Använd **Get-AzApiManagementOpenIdConnectProviderClientSecret** för att få klient hemlighet.</span><span class="sxs-lookup"><span data-stu-id="2a656-111">To get client secret, use **Get-AzApiManagementOpenIdConnectProviderClientSecret**.</span></span>

## <span data-ttu-id="2a656-112">BESKRIVS</span><span class="sxs-lookup"><span data-stu-id="2a656-112">EXAMPLES</span></span>

### <span data-ttu-id="2a656-113">Exempel 1: Hämta alla leverantörer</span><span class="sxs-lookup"><span data-stu-id="2a656-113">Example 1: Get all providers</span></span>
```
PS C:\>$apimContext = New-AzApiManagementContext -ResourceGroupName "Api-Default-WestUS" -ServiceName "contoso"
PS C:\>Get-AzApiManagementOpenIdConnectProvider -Context $apimContext
```

<span data-ttu-id="2a656-114">Det här kommandot får alla OpenID Connect-leverantörer för angiven kontext.</span><span class="sxs-lookup"><span data-stu-id="2a656-114">This command gets all OpenID Connect providers for the specified context.</span></span>

### <span data-ttu-id="2a656-115">Exempel 2: skaffa en leverantör med hjälp av ett ID</span><span class="sxs-lookup"><span data-stu-id="2a656-115">Example 2: Get a provider by using an ID</span></span>
```
PS C:\>$apimContext = New-AzApiManagementContext -ResourceGroupName "Api-Default-WestUS" -ServiceName "contoso"
PS C:\>Get-AzApiManagementOpenIdConnectProvider -Context $apimContext -OpenIdConnectProviderId "OICProvider01"
```

<span data-ttu-id="2a656-116">Det här kommandot får leverantören med ID-OICProvider01.</span><span class="sxs-lookup"><span data-stu-id="2a656-116">This command gets the provider that has the ID OICProvider01.</span></span>

### <span data-ttu-id="2a656-117">Exempel 3: skaffa en leverantör genom att använda ett namn</span><span class="sxs-lookup"><span data-stu-id="2a656-117">Example 3: Get a provider by using a name</span></span>
```
PS C:\>$apimContext = New-AzApiManagementContext -ResourceGroupName "Api-Default-WestUS" -ServiceName "contoso"
PS C:\>Get-AzApiManagementOpenIdConnectProvider -Context $apimContext -Name "Contoso OpenID Connect Provider"
```

<span data-ttu-id="2a656-118">Med det här kommandot hämtas leverantören Contoso OpenID Connect-leverantör.</span><span class="sxs-lookup"><span data-stu-id="2a656-118">This command gets the provider named Contoso OpenID Connect Provider.</span></span>

## <span data-ttu-id="2a656-119">MALLPARAMETRAR</span><span class="sxs-lookup"><span data-stu-id="2a656-119">PARAMETERS</span></span>

### <span data-ttu-id="2a656-120">-Kontext</span><span class="sxs-lookup"><span data-stu-id="2a656-120">-Context</span></span>
<span data-ttu-id="2a656-121">Anger ett **PsApiManagementContext** -objekt.</span><span class="sxs-lookup"><span data-stu-id="2a656-121">Specifies a **PsApiManagementContext** object.</span></span>

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

### <span data-ttu-id="2a656-122">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="2a656-122">-DefaultProfile</span></span>
<span data-ttu-id="2a656-123">Autentiseringsuppgifter, konto, klient organisation och abonnemang som används för kommunikation med Azure.</span><span class="sxs-lookup"><span data-stu-id="2a656-123">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="2a656-124">-Namn</span><span class="sxs-lookup"><span data-stu-id="2a656-124">-Name</span></span>
<span data-ttu-id="2a656-125">Anger ett eget namn på en leverantör.</span><span class="sxs-lookup"><span data-stu-id="2a656-125">Specifies a friendly name of a provider.</span></span>
<span data-ttu-id="2a656-126">Om du anger ett namn blir denna cmdlet den leverantören.</span><span class="sxs-lookup"><span data-stu-id="2a656-126">If you specify a name, this cmdlet gets that provider.</span></span>

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

### <span data-ttu-id="2a656-127">-OpenIdConnectProviderId</span><span class="sxs-lookup"><span data-stu-id="2a656-127">-OpenIdConnectProviderId</span></span>
<span data-ttu-id="2a656-128">Anger ett ID för den provider som denna cmdlet tar bort.</span><span class="sxs-lookup"><span data-stu-id="2a656-128">Specifies an ID of the provider that this cmdlet removes.</span></span>
<span data-ttu-id="2a656-129">Om du anger ett ID får denna cmdlet den leverantören.</span><span class="sxs-lookup"><span data-stu-id="2a656-129">If you specify an ID, this cmdlet gets that provider.</span></span>

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

### <span data-ttu-id="2a656-130">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="2a656-130">CommonParameters</span></span>
<span data-ttu-id="2a656-131">Den här cmdleten har stöd för de gemensamma parametrarna:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-disvariable,-utbuffer,-PipelineVariable,-verbose,-WarningAction och-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="2a656-131">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="2a656-132">Mer information finns i [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="2a656-132">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="2a656-133">KOSTNADS</span><span class="sxs-lookup"><span data-stu-id="2a656-133">INPUTS</span></span>

### <span data-ttu-id="2a656-134">Microsoft. Azure. commands. ApiManagement. ServiceManagement. Models. PsApiManagementContext</span><span class="sxs-lookup"><span data-stu-id="2a656-134">Microsoft.Azure.Commands.ApiManagement.ServiceManagement.Models.PsApiManagementContext</span></span>

### <span data-ttu-id="2a656-135">System. String</span><span class="sxs-lookup"><span data-stu-id="2a656-135">System.String</span></span>

## <span data-ttu-id="2a656-136">VÄRDEN</span><span class="sxs-lookup"><span data-stu-id="2a656-136">OUTPUTS</span></span>

### <span data-ttu-id="2a656-137">Microsoft. Azure. commands. ApiManagement. ServiceManagement. Models. PsApiManagementOpenIdConnectProvider</span><span class="sxs-lookup"><span data-stu-id="2a656-137">Microsoft.Azure.Commands.ApiManagement.ServiceManagement.Models.PsApiManagementOpenIdConnectProvider</span></span>

## <span data-ttu-id="2a656-138">ANMÄRKNINGAR</span><span class="sxs-lookup"><span data-stu-id="2a656-138">NOTES</span></span>

## <span data-ttu-id="2a656-139">RELATERADE LÄNKAR</span><span class="sxs-lookup"><span data-stu-id="2a656-139">RELATED LINKS</span></span>

[<span data-ttu-id="2a656-140">New-AzApiManagementOpenIdConnectProvider</span><span class="sxs-lookup"><span data-stu-id="2a656-140">New-AzApiManagementOpenIdConnectProvider</span></span>](./New-AzApiManagementOpenIdConnectProvider.md)

[<span data-ttu-id="2a656-141">Remove-AzApiManagementOpenIdConnectProvider</span><span class="sxs-lookup"><span data-stu-id="2a656-141">Remove-AzApiManagementOpenIdConnectProvider</span></span>](./Remove-AzApiManagementOpenIdConnectProvider.md)

[<span data-ttu-id="2a656-142">Set-AzApiManagementOpenIdConnectProvider</span><span class="sxs-lookup"><span data-stu-id="2a656-142">Set-AzApiManagementOpenIdConnectProvider</span></span>](./Set-AzApiManagementOpenIdConnectProvider.md)

