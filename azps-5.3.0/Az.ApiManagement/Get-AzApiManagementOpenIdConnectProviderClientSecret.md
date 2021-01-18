---
external help file: Microsoft.Azure.PowerShell.Cmdlets.ApiManagement.ServiceManagement.dll-Help.xml
Module Name: Az.ApiManagement
online version: https://docs.microsoft.com/en-us/powershell/module/az.apimanagement/get-azapimanagementopenidconnectproviderclientsecret
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/ApiManagement/ApiManagement/help/Get-AzApiManagementOpenIdConnectProviderClientSecret.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/ApiManagement/ApiManagement/help/Get-AzApiManagementOpenIdConnectProviderClientSecret.md
ms.openlocfilehash: dcc66b6d28157ff9d5551e2fdf0cab18f7727828
ms.sourcegitcommit: 68451baa389791703e666d95469602c5652609ee
ms.translationtype: MT
ms.contentlocale: sv-SE
ms.lasthandoff: 01/05/2021
ms.locfileid: "98525088"
---
# <span data-ttu-id="0a8a4-101">Get-AzApiManagementOpenIdConnectProviderClientSecret</span><span class="sxs-lookup"><span data-stu-id="0a8a4-101">Get-AzApiManagementOpenIdConnectProviderClientSecret</span></span>

## <span data-ttu-id="0a8a4-102">Sammanfattning</span><span class="sxs-lookup"><span data-stu-id="0a8a4-102">SYNOPSIS</span></span>
<span data-ttu-id="0a8a4-103">Hämtar OpenID för klient hemlighet.</span><span class="sxs-lookup"><span data-stu-id="0a8a4-103">Gets OpenID Connect provider client secret.</span></span>

## <span data-ttu-id="0a8a4-104">FRÅGESYNTAXEN</span><span class="sxs-lookup"><span data-stu-id="0a8a4-104">SYNTAX</span></span>

```
Get-AzApiManagementOpenIdConnectProviderClientSecret -Context <PsApiManagementContext>
 -OpenIdConnectProviderId <String> [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="0a8a4-105">PROBLEMBESKRIVNING</span><span class="sxs-lookup"><span data-stu-id="0a8a4-105">DESCRIPTION</span></span>
<span data-ttu-id="0a8a4-106">Hämtar OpenID för klient hemlighet.</span><span class="sxs-lookup"><span data-stu-id="0a8a4-106">Gets OpenID Connect provider client secret.</span></span>

## <span data-ttu-id="0a8a4-107">BESKRIVS</span><span class="sxs-lookup"><span data-stu-id="0a8a4-107">EXAMPLES</span></span>

### <span data-ttu-id="0a8a4-108">Exempel 1: skaffa en leverantörs klient hemlighet genom att använda ett ID</span><span class="sxs-lookup"><span data-stu-id="0a8a4-108">Example 1: Get a provider client secret by using an ID</span></span>
```
PS C:\>$apimContext = New-AzApiManagementContext -ResourceGroupName "Api-Default-WestUS" -ServiceName "contoso"
PS C:\>Get-AzApiManagementOpenIdConnectProviderClientSecret -Context $apimContext -OpenIdConnectProviderId "OICProvider01"
```

<span data-ttu-id="0a8a4-109">Det här kommandot får en klient hemlighet för den provider som har ID-OICProvider01.</span><span class="sxs-lookup"><span data-stu-id="0a8a4-109">This command gets a client secret of the provider that has the ID OICProvider01.</span></span>

## <span data-ttu-id="0a8a4-110">MALLPARAMETRAR</span><span class="sxs-lookup"><span data-stu-id="0a8a4-110">PARAMETERS</span></span>

### <span data-ttu-id="0a8a4-111">-Kontext</span><span class="sxs-lookup"><span data-stu-id="0a8a4-111">-Context</span></span>
<span data-ttu-id="0a8a4-112">Instans av PsApiManagementContext.</span><span class="sxs-lookup"><span data-stu-id="0a8a4-112">Instance of PsApiManagementContext.</span></span>
<span data-ttu-id="0a8a4-113">Denna parameter är obligatorisk.</span><span class="sxs-lookup"><span data-stu-id="0a8a4-113">This parameter is required.</span></span>

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

### <span data-ttu-id="0a8a4-114">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="0a8a4-114">-DefaultProfile</span></span>
<span data-ttu-id="0a8a4-115">Autentiseringsuppgifter, konto, klient organisation och abonnemang som används för kommunikation med Azure.</span><span class="sxs-lookup"><span data-stu-id="0a8a4-115">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="0a8a4-116">-OpenIdConnectProviderId</span><span class="sxs-lookup"><span data-stu-id="0a8a4-116">-OpenIdConnectProviderId</span></span>
<span data-ttu-id="0a8a4-117">Identifierare för en OpenID Connect-leverantör.</span><span class="sxs-lookup"><span data-stu-id="0a8a4-117">Identifier of a OpenID Connect Provider.</span></span>
<span data-ttu-id="0a8a4-118">Denna parameter är obligatorisk.</span><span class="sxs-lookup"><span data-stu-id="0a8a4-118">This parameter is required.</span></span>

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

### <span data-ttu-id="0a8a4-119">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="0a8a4-119">CommonParameters</span></span>
<span data-ttu-id="0a8a4-120">Den här cmdleten har stöd för de gemensamma parametrarna:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-disvariable,-utbuffer,-PipelineVariable,-verbose,-WarningAction och-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="0a8a4-120">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="0a8a4-121">Mer information finns i [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="0a8a4-121">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="0a8a4-122">KOSTNADS</span><span class="sxs-lookup"><span data-stu-id="0a8a4-122">INPUTS</span></span>

### <span data-ttu-id="0a8a4-123">Microsoft. Azure. commands. ApiManagement. ServiceManagement. Models. PsApiManagementContext</span><span class="sxs-lookup"><span data-stu-id="0a8a4-123">Microsoft.Azure.Commands.ApiManagement.ServiceManagement.Models.PsApiManagementContext</span></span>

### <span data-ttu-id="0a8a4-124">System. String</span><span class="sxs-lookup"><span data-stu-id="0a8a4-124">System.String</span></span>

## <span data-ttu-id="0a8a4-125">VÄRDEN</span><span class="sxs-lookup"><span data-stu-id="0a8a4-125">OUTPUTS</span></span>

### <span data-ttu-id="0a8a4-126">Microsoft. Azure. commands. ApiManagement. ServiceManagement. Models. PsApiManagementClientSecret</span><span class="sxs-lookup"><span data-stu-id="0a8a4-126">Microsoft.Azure.Commands.ApiManagement.ServiceManagement.Models.PsApiManagementClientSecret</span></span>

## <span data-ttu-id="0a8a4-127">ANMÄRKNINGAR</span><span class="sxs-lookup"><span data-stu-id="0a8a4-127">NOTES</span></span>

## <span data-ttu-id="0a8a4-128">RELATERADE LÄNKAR</span><span class="sxs-lookup"><span data-stu-id="0a8a4-128">RELATED LINKS</span></span>
