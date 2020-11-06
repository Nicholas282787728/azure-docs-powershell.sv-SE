---
external help file: Microsoft.Azure.Commands.ApiManagement.ServiceManagement.dll-Help.xml
Module Name: AzureRM.ApiManagement
ms.assetid: 15B6EAE2-56ED-4A01-B8EA-52B9FCDC1F66
online version: ''
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/ApiManagement/Commands.ApiManagement/help/Get-AzureRmApiManagementOpenIdConnectProvider.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/ApiManagement/Commands.ApiManagement/help/Get-AzureRmApiManagementOpenIdConnectProvider.md
ms.openlocfilehash: d97090f6374890d9ae7ba24e53d6e1d60430f7b0
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: sv-SE
ms.lasthandoff: 08/20/2020
ms.locfileid: "93573779"
---
# <span data-ttu-id="1a62b-101">Get-AzureRmApiManagementOpenIdConnectProvider</span><span class="sxs-lookup"><span data-stu-id="1a62b-101">Get-AzureRmApiManagementOpenIdConnectProvider</span></span>

## <span data-ttu-id="1a62b-102">Sammanfattning</span><span class="sxs-lookup"><span data-stu-id="1a62b-102">SYNOPSIS</span></span>
<span data-ttu-id="1a62b-103">Hämtar OpenID.</span><span class="sxs-lookup"><span data-stu-id="1a62b-103">Gets OpenID Connect providers.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="1a62b-104">FRÅGESYNTAXEN</span><span class="sxs-lookup"><span data-stu-id="1a62b-104">SYNTAX</span></span>

### <span data-ttu-id="1a62b-105">Skaffa alla OpenID Connect-leverantörer (standard)</span><span class="sxs-lookup"><span data-stu-id="1a62b-105">Get all OpenID Connect Providers (Default)</span></span>
```
Get-AzureRmApiManagementOpenIdConnectProvider -Context <PsApiManagementContext>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="1a62b-106">Få med OpenID Connect-ID</span><span class="sxs-lookup"><span data-stu-id="1a62b-106">Get by OpenID Connect Provider ID</span></span>
```
Get-AzureRmApiManagementOpenIdConnectProvider -Context <PsApiManagementContext>
 [-OpenIdConnectProviderId <String>] [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="1a62b-107">Sök efter eget namn för OpenID</span><span class="sxs-lookup"><span data-stu-id="1a62b-107">Find by OpenID Connect Provider friendly Name</span></span>
```
Get-AzureRmApiManagementOpenIdConnectProvider -Context <PsApiManagementContext> [-Name <String>]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="1a62b-108">PROBLEMBESKRIVNING</span><span class="sxs-lookup"><span data-stu-id="1a62b-108">DESCRIPTION</span></span>
<span data-ttu-id="1a62b-109">Cmdleten **Get-AzureRmApiManagementOpenIdConnectProvider** hämtar OpenID Connect-leverantörer i Azure API Management.</span><span class="sxs-lookup"><span data-stu-id="1a62b-109">The **Get-AzureRmApiManagementOpenIdConnectProvider** cmdlet gets OpenID Connect providers in Azure API Management.</span></span>

## <span data-ttu-id="1a62b-110">BESKRIVS</span><span class="sxs-lookup"><span data-stu-id="1a62b-110">EXAMPLES</span></span>

### <span data-ttu-id="1a62b-111">Exempel 1: Hämta alla leverantörer</span><span class="sxs-lookup"><span data-stu-id="1a62b-111">Example 1: Get all providers</span></span>
```
PS C:\>Get-AzureRmApiManagementOpenIdConnectProvider -Context $ApimContext
```

<span data-ttu-id="1a62b-112">Det här kommandot får alla OpenID Connect-leverantörer för angiven kontext.</span><span class="sxs-lookup"><span data-stu-id="1a62b-112">This command gets all OpenID Connect providers for the specified context.</span></span>

### <span data-ttu-id="1a62b-113">Exempel 2: skaffa en leverantör med hjälp av ett ID</span><span class="sxs-lookup"><span data-stu-id="1a62b-113">Example 2: Get a provider by using an ID</span></span>
```
PS C:\>Get-AzureRmApiManagementOpenIdConnectProvider -Context $ApimContext -OpenIdConnectProviderId "OICProvicer01"
```

<span data-ttu-id="1a62b-114">Det här kommandot får leverantören med ID-OICProvicer01.</span><span class="sxs-lookup"><span data-stu-id="1a62b-114">This command gets the provider that has the ID OICProvicer01.</span></span>

### <span data-ttu-id="1a62b-115">Exempel 3: skaffa en leverantör genom att använda ett namn</span><span class="sxs-lookup"><span data-stu-id="1a62b-115">Example 3: Get a provider by using a name</span></span>
```
PS C:\>Get-AzureRmApiManagementOpenIdConnectProvider -Context $ApimContext -Name "Contoso OpenID Connect Provider"
```

<span data-ttu-id="1a62b-116">Med det här kommandot hämtas leverantören Contoso OpenID Connect-leverantör.</span><span class="sxs-lookup"><span data-stu-id="1a62b-116">This command gets the provider named Contoso OpenID Connect Provider.</span></span>

## <span data-ttu-id="1a62b-117">MALLPARAMETRAR</span><span class="sxs-lookup"><span data-stu-id="1a62b-117">PARAMETERS</span></span>

### <span data-ttu-id="1a62b-118">-Kontext</span><span class="sxs-lookup"><span data-stu-id="1a62b-118">-Context</span></span>
<span data-ttu-id="1a62b-119">Anger ett **PsApiManagementContext** -objekt.</span><span class="sxs-lookup"><span data-stu-id="1a62b-119">Specifies a **PsApiManagementContext** object.</span></span>

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

### <span data-ttu-id="1a62b-120">-Namn</span><span class="sxs-lookup"><span data-stu-id="1a62b-120">-Name</span></span>
<span data-ttu-id="1a62b-121">Anger ett eget namn på en leverantör.</span><span class="sxs-lookup"><span data-stu-id="1a62b-121">Specifies a friendly name of a provider.</span></span>
<span data-ttu-id="1a62b-122">Om du anger ett namn blir denna cmdlet den leverantören.</span><span class="sxs-lookup"><span data-stu-id="1a62b-122">If you specify a name, this cmdlet gets that provider.</span></span>

```yaml
Type: System.String
Parameter Sets: Find by OpenID Connect Provider friendly Name
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="1a62b-123">-OpenIdConnectProviderId</span><span class="sxs-lookup"><span data-stu-id="1a62b-123">-OpenIdConnectProviderId</span></span>
<span data-ttu-id="1a62b-124">Anger ett ID för den provider som denna cmdlet tar bort.</span><span class="sxs-lookup"><span data-stu-id="1a62b-124">Specifies an ID of the provider that this cmdlet removes.</span></span>
<span data-ttu-id="1a62b-125">Om du anger ett ID får denna cmdlet den leverantören.</span><span class="sxs-lookup"><span data-stu-id="1a62b-125">If you specify an ID, this cmdlet gets that provider.</span></span>

```yaml
Type: System.String
Parameter Sets: Get by OpenID Connect Provider ID
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="1a62b-126">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="1a62b-126">-DefaultProfile</span></span>
<span data-ttu-id="1a62b-127">Autentiseringsuppgifter, konto, klient organisation och abonnemang som används för kommunikation med Azure.</span><span class="sxs-lookup"><span data-stu-id="1a62b-127">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="1a62b-128">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="1a62b-128">CommonParameters</span></span>
<span data-ttu-id="1a62b-129">Den här cmdleten har stöd för de gemensamma parametrarna:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-disvariable,-utbuffer,-PipelineVariable,-verbose,-WarningAction och-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="1a62b-129">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="1a62b-130">Mer information finns i about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="1a62b-130">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="1a62b-131">KOSTNADS</span><span class="sxs-lookup"><span data-stu-id="1a62b-131">INPUTS</span></span>

## <span data-ttu-id="1a62b-132">VÄRDEN</span><span class="sxs-lookup"><span data-stu-id="1a62b-132">OUTPUTS</span></span>

### <span data-ttu-id="1a62b-133">IList<Microsoft. Azure. commands. ApiManagement. ServiceManagement. Models. PsApiManagementOpenIdConnectProvider></span><span class="sxs-lookup"><span data-stu-id="1a62b-133">IList<Microsoft.Azure.Commands.ApiManagement.ServiceManagement.Models.PsApiManagementOpenIdConnectProvider></span></span>

## <span data-ttu-id="1a62b-134">ANMÄRKNINGAR</span><span class="sxs-lookup"><span data-stu-id="1a62b-134">NOTES</span></span>

## <span data-ttu-id="1a62b-135">RELATERADE LÄNKAR</span><span class="sxs-lookup"><span data-stu-id="1a62b-135">RELATED LINKS</span></span>

[<span data-ttu-id="1a62b-136">New-AzureRmApiManagementOpenIdConnectProvider</span><span class="sxs-lookup"><span data-stu-id="1a62b-136">New-AzureRmApiManagementOpenIdConnectProvider</span></span>](./New-AzureRmApiManagementOpenIdConnectProvider.md)

[<span data-ttu-id="1a62b-137">Remove-AzureRmApiManagementOpenIdConnectProvider</span><span class="sxs-lookup"><span data-stu-id="1a62b-137">Remove-AzureRmApiManagementOpenIdConnectProvider</span></span>](./Remove-AzureRmApiManagementOpenIdConnectProvider.md)

[<span data-ttu-id="1a62b-138">Set-AzureRmApiManagementOpenIdConnectProvider</span><span class="sxs-lookup"><span data-stu-id="1a62b-138">Set-AzureRmApiManagementOpenIdConnectProvider</span></span>](./Set-AzureRmApiManagementOpenIdConnectProvider.md)


