---
external help file: Microsoft.Azure.PowerShell.Cmdlets.ApiManagement.ServiceManagement.dll-Help.xml
Module Name: Az.ApiManagement
online version: https://docs.microsoft.com/en-us/powershell/module/az.apimanagement/get-azapimanagementidentityproviderclientsecret
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/ApiManagement/ApiManagement/help/Get-AzApiManagementIdentityProviderClientSecret.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/ApiManagement/ApiManagement/help/Get-AzApiManagementIdentityProviderClientSecret.md
ms.openlocfilehash: d75d385bc158e0855601d3432dff79b2e4339f2f
ms.sourcegitcommit: 1de2b6c3c99197958fa2101bc37680e7507f91ac
ms.translationtype: MT
ms.contentlocale: sv-SE
ms.lasthandoff: 10/13/2020
ms.locfileid: "94101791"
---
# <span data-ttu-id="2dcad-101">Get-AzApiManagementIdentityProviderClientSecret</span><span class="sxs-lookup"><span data-stu-id="2dcad-101">Get-AzApiManagementIdentityProviderClientSecret</span></span>

## <span data-ttu-id="2dcad-102">Sammanfattning</span><span class="sxs-lookup"><span data-stu-id="2dcad-102">SYNOPSIS</span></span>
<span data-ttu-id="2dcad-103">Skaffa klient hemlighet för identitets leverantör.</span><span class="sxs-lookup"><span data-stu-id="2dcad-103">Get the identity provider client secret.</span></span>

## <span data-ttu-id="2dcad-104">FRÅGESYNTAXEN</span><span class="sxs-lookup"><span data-stu-id="2dcad-104">SYNTAX</span></span>

```
Get-AzApiManagementIdentityProviderClientSecret -Context <PsApiManagementContext>
 -Type <PsApiManagementIdentityProviderType> [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="2dcad-105">PROBLEMBESKRIVNING</span><span class="sxs-lookup"><span data-stu-id="2dcad-105">DESCRIPTION</span></span>
<span data-ttu-id="2dcad-106">Skaffa klient hemlighet för identitets leverantör.</span><span class="sxs-lookup"><span data-stu-id="2dcad-106">Get the identity provider client secret.</span></span>

## <span data-ttu-id="2dcad-107">BESKRIVS</span><span class="sxs-lookup"><span data-stu-id="2dcad-107">EXAMPLES</span></span>

### <span data-ttu-id="2dcad-108">Exempel 1: Hämta klient hemligheten för AAD-typ identitets leverantör</span><span class="sxs-lookup"><span data-stu-id="2dcad-108">Example 1: Get the client secret of AAD Type Identity Provider</span></span>
```powershell
PS C:\>$apimContext = New-AzApiManagementContext -ResourceGroupName "Api-Default-WestUS" -ServiceName "contoso"
PS C:\> Get-AzApiManagementIdentityProviderClientSecret -Context $apimContext -Type Aad
```

<span data-ttu-id="2dcad-109">Hämtar klient hemligheten för identitets konfiguration för Azure Active Directory.</span><span class="sxs-lookup"><span data-stu-id="2dcad-109">Gets the client secret of the Identity Provider Configuration of Azure Active Directory.</span></span>

## <span data-ttu-id="2dcad-110">MALLPARAMETRAR</span><span class="sxs-lookup"><span data-stu-id="2dcad-110">PARAMETERS</span></span>

### <span data-ttu-id="2dcad-111">-Kontext</span><span class="sxs-lookup"><span data-stu-id="2dcad-111">-Context</span></span>
<span data-ttu-id="2dcad-112">Instans av PsApiManagementContext.</span><span class="sxs-lookup"><span data-stu-id="2dcad-112">Instance of PsApiManagementContext.</span></span>
<span data-ttu-id="2dcad-113">Denna parameter är obligatorisk.</span><span class="sxs-lookup"><span data-stu-id="2dcad-113">This parameter is required.</span></span>

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

### <span data-ttu-id="2dcad-114">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="2dcad-114">-DefaultProfile</span></span>
<span data-ttu-id="2dcad-115">Autentiseringsuppgifter, konto, klient organisation och abonnemang som används för kommunikation med Azure.</span><span class="sxs-lookup"><span data-stu-id="2dcad-115">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="2dcad-116">– Skriv</span><span class="sxs-lookup"><span data-stu-id="2dcad-116">-Type</span></span>
<span data-ttu-id="2dcad-117">Identifierare för en identitets leverantör.</span><span class="sxs-lookup"><span data-stu-id="2dcad-117">Identifier of a Identity Provider.</span></span>
<span data-ttu-id="2dcad-118">Denna parameter är obligatorisk.</span><span class="sxs-lookup"><span data-stu-id="2dcad-118">This parameter is required.</span></span>

```yaml
Type: Microsoft.Azure.Commands.ApiManagement.ServiceManagement.Models.PsApiManagementIdentityProviderType
Parameter Sets: (All)
Aliases:
Accepted values: Facebook, Google, Microsoft, Twitter, Aad, AadB2C

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="2dcad-119">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="2dcad-119">CommonParameters</span></span>
<span data-ttu-id="2dcad-120">Den här cmdleten har stöd för de gemensamma parametrarna:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-disvariable,-utbuffer,-PipelineVariable,-verbose,-WarningAction och-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="2dcad-120">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="2dcad-121">Mer information finns i [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="2dcad-121">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="2dcad-122">KOSTNADS</span><span class="sxs-lookup"><span data-stu-id="2dcad-122">INPUTS</span></span>

### <span data-ttu-id="2dcad-123">Microsoft. Azure. commands. ApiManagement. ServiceManagement. Models. PsApiManagementContext</span><span class="sxs-lookup"><span data-stu-id="2dcad-123">Microsoft.Azure.Commands.ApiManagement.ServiceManagement.Models.PsApiManagementContext</span></span>

### <span data-ttu-id="2dcad-124">Microsoft. Azure. commands. ApiManagement. ServiceManagement. Models. PsApiManagementIdentityProviderType</span><span class="sxs-lookup"><span data-stu-id="2dcad-124">Microsoft.Azure.Commands.ApiManagement.ServiceManagement.Models.PsApiManagementIdentityProviderType</span></span>

## <span data-ttu-id="2dcad-125">VÄRDEN</span><span class="sxs-lookup"><span data-stu-id="2dcad-125">OUTPUTS</span></span>

### <span data-ttu-id="2dcad-126">Microsoft. Azure. commands. ApiManagement. ServiceManagement. Models. PsApiManagementClientSecret</span><span class="sxs-lookup"><span data-stu-id="2dcad-126">Microsoft.Azure.Commands.ApiManagement.ServiceManagement.Models.PsApiManagementClientSecret</span></span>

## <span data-ttu-id="2dcad-127">ANMÄRKNINGAR</span><span class="sxs-lookup"><span data-stu-id="2dcad-127">NOTES</span></span>

## <span data-ttu-id="2dcad-128">RELATERADE LÄNKAR</span><span class="sxs-lookup"><span data-stu-id="2dcad-128">RELATED LINKS</span></span>
