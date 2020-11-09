---
external help file: Microsoft.Azure.PowerShell.Cmdlets.ApiManagement.ServiceManagement.dll-Help.xml
Module Name: Az.ApiManagement
online version: https://docs.microsoft.com/en-us/powershell/module/az.apimanagement/get-azapimanagementidentityproviderclientsecret
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/ApiManagement/ApiManagement/help/Get-AzApiManagementIdentityProviderClientSecret.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/ApiManagement/ApiManagement/help/Get-AzApiManagementIdentityProviderClientSecret.md
ms.openlocfilehash: d75d385bc158e0855601d3432dff79b2e4339f2f
ms.sourcegitcommit: b4a38bcb0501a9016a4998efd377aa75d3ef9ce8
ms.translationtype: MT
ms.contentlocale: sv-SE
ms.lasthandoff: 10/27/2020
ms.locfileid: "94321932"
---
# <span data-ttu-id="ed3fe-101">Get-AzApiManagementIdentityProviderClientSecret</span><span class="sxs-lookup"><span data-stu-id="ed3fe-101">Get-AzApiManagementIdentityProviderClientSecret</span></span>

## <span data-ttu-id="ed3fe-102">Sammanfattning</span><span class="sxs-lookup"><span data-stu-id="ed3fe-102">SYNOPSIS</span></span>
<span data-ttu-id="ed3fe-103">Skaffa klient hemlighet för identitets leverantör.</span><span class="sxs-lookup"><span data-stu-id="ed3fe-103">Get the identity provider client secret.</span></span>

## <span data-ttu-id="ed3fe-104">FRÅGESYNTAXEN</span><span class="sxs-lookup"><span data-stu-id="ed3fe-104">SYNTAX</span></span>

```
Get-AzApiManagementIdentityProviderClientSecret -Context <PsApiManagementContext>
 -Type <PsApiManagementIdentityProviderType> [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="ed3fe-105">PROBLEMBESKRIVNING</span><span class="sxs-lookup"><span data-stu-id="ed3fe-105">DESCRIPTION</span></span>
<span data-ttu-id="ed3fe-106">Skaffa klient hemlighet för identitets leverantör.</span><span class="sxs-lookup"><span data-stu-id="ed3fe-106">Get the identity provider client secret.</span></span>

## <span data-ttu-id="ed3fe-107">BESKRIVS</span><span class="sxs-lookup"><span data-stu-id="ed3fe-107">EXAMPLES</span></span>

### <span data-ttu-id="ed3fe-108">Exempel 1: Hämta klient hemligheten för AAD-typ identitets leverantör</span><span class="sxs-lookup"><span data-stu-id="ed3fe-108">Example 1: Get the client secret of AAD Type Identity Provider</span></span>
```powershell
PS C:\>$apimContext = New-AzApiManagementContext -ResourceGroupName "Api-Default-WestUS" -ServiceName "contoso"
PS C:\> Get-AzApiManagementIdentityProviderClientSecret -Context $apimContext -Type Aad
```

<span data-ttu-id="ed3fe-109">Hämtar klient hemligheten för identitets konfiguration för Azure Active Directory.</span><span class="sxs-lookup"><span data-stu-id="ed3fe-109">Gets the client secret of the Identity Provider Configuration of Azure Active Directory.</span></span>

## <span data-ttu-id="ed3fe-110">MALLPARAMETRAR</span><span class="sxs-lookup"><span data-stu-id="ed3fe-110">PARAMETERS</span></span>

### <span data-ttu-id="ed3fe-111">-Kontext</span><span class="sxs-lookup"><span data-stu-id="ed3fe-111">-Context</span></span>
<span data-ttu-id="ed3fe-112">Instans av PsApiManagementContext.</span><span class="sxs-lookup"><span data-stu-id="ed3fe-112">Instance of PsApiManagementContext.</span></span>
<span data-ttu-id="ed3fe-113">Denna parameter är obligatorisk.</span><span class="sxs-lookup"><span data-stu-id="ed3fe-113">This parameter is required.</span></span>

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

### <span data-ttu-id="ed3fe-114">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="ed3fe-114">-DefaultProfile</span></span>
<span data-ttu-id="ed3fe-115">Autentiseringsuppgifter, konto, klient organisation och abonnemang som används för kommunikation med Azure.</span><span class="sxs-lookup"><span data-stu-id="ed3fe-115">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="ed3fe-116">– Skriv</span><span class="sxs-lookup"><span data-stu-id="ed3fe-116">-Type</span></span>
<span data-ttu-id="ed3fe-117">Identifierare för en identitets leverantör.</span><span class="sxs-lookup"><span data-stu-id="ed3fe-117">Identifier of a Identity Provider.</span></span>
<span data-ttu-id="ed3fe-118">Denna parameter är obligatorisk.</span><span class="sxs-lookup"><span data-stu-id="ed3fe-118">This parameter is required.</span></span>

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

### <span data-ttu-id="ed3fe-119">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="ed3fe-119">CommonParameters</span></span>
<span data-ttu-id="ed3fe-120">Den här cmdleten har stöd för de gemensamma parametrarna:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-disvariable,-utbuffer,-PipelineVariable,-verbose,-WarningAction och-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="ed3fe-120">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="ed3fe-121">Mer information finns i [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="ed3fe-121">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="ed3fe-122">KOSTNADS</span><span class="sxs-lookup"><span data-stu-id="ed3fe-122">INPUTS</span></span>

### <span data-ttu-id="ed3fe-123">Microsoft. Azure. commands. ApiManagement. ServiceManagement. Models. PsApiManagementContext</span><span class="sxs-lookup"><span data-stu-id="ed3fe-123">Microsoft.Azure.Commands.ApiManagement.ServiceManagement.Models.PsApiManagementContext</span></span>

### <span data-ttu-id="ed3fe-124">Microsoft. Azure. commands. ApiManagement. ServiceManagement. Models. PsApiManagementIdentityProviderType</span><span class="sxs-lookup"><span data-stu-id="ed3fe-124">Microsoft.Azure.Commands.ApiManagement.ServiceManagement.Models.PsApiManagementIdentityProviderType</span></span>

## <span data-ttu-id="ed3fe-125">VÄRDEN</span><span class="sxs-lookup"><span data-stu-id="ed3fe-125">OUTPUTS</span></span>

### <span data-ttu-id="ed3fe-126">Microsoft. Azure. commands. ApiManagement. ServiceManagement. Models. PsApiManagementClientSecret</span><span class="sxs-lookup"><span data-stu-id="ed3fe-126">Microsoft.Azure.Commands.ApiManagement.ServiceManagement.Models.PsApiManagementClientSecret</span></span>

## <span data-ttu-id="ed3fe-127">ANMÄRKNINGAR</span><span class="sxs-lookup"><span data-stu-id="ed3fe-127">NOTES</span></span>

## <span data-ttu-id="ed3fe-128">RELATERADE LÄNKAR</span><span class="sxs-lookup"><span data-stu-id="ed3fe-128">RELATED LINKS</span></span>
