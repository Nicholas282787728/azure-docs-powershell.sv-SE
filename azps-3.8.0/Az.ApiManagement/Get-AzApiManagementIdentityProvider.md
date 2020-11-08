---
external help file: Microsoft.Azure.PowerShell.Cmdlets.ApiManagement.ServiceManagement.dll-Help.xml
Module Name: Az.ApiManagement
online version: https://docs.microsoft.com/en-us/powershell/module/az.apimanagement/get-azapimanagementidentityprovider
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/ApiManagement/ApiManagement/help/Get-AzApiManagementIdentityProvider.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/ApiManagement/ApiManagement/help/Get-AzApiManagementIdentityProvider.md
ms.openlocfilehash: 75525d3c77c3e2113c0e3cff5a7741ab916d7485
ms.sourcegitcommit: 6a91b4c545350d316d3cf8c62f384478e3f3ba24
ms.translationtype: MT
ms.contentlocale: sv-SE
ms.lasthandoff: 04/21/2020
ms.locfileid: "94089659"
---
# <span data-ttu-id="63d43-101">Get-AzApiManagementIdentityProvider</span><span class="sxs-lookup"><span data-stu-id="63d43-101">Get-AzApiManagementIdentityProvider</span></span>

## <span data-ttu-id="63d43-102">Sammanfattning</span><span class="sxs-lookup"><span data-stu-id="63d43-102">SYNOPSIS</span></span>
<span data-ttu-id="63d43-103">Hämta information om identitets leverantörens konfiguration.</span><span class="sxs-lookup"><span data-stu-id="63d43-103">Get the identity provider configuration details.</span></span>

## <span data-ttu-id="63d43-104">FRÅGESYNTAXEN</span><span class="sxs-lookup"><span data-stu-id="63d43-104">SYNTAX</span></span>

### <span data-ttu-id="63d43-105">AllIdentityProviders (standard)</span><span class="sxs-lookup"><span data-stu-id="63d43-105">AllIdentityProviders (Default)</span></span>
```
Get-AzApiManagementIdentityProvider -Context <PsApiManagementContext>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="63d43-106">IdentityProviderByType</span><span class="sxs-lookup"><span data-stu-id="63d43-106">IdentityProviderByType</span></span>
```
Get-AzApiManagementIdentityProvider -Context <PsApiManagementContext>
 -Type <PsApiManagementIdentityProviderType> [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="63d43-107">PROBLEMBESKRIVNING</span><span class="sxs-lookup"><span data-stu-id="63d43-107">DESCRIPTION</span></span>
<span data-ttu-id="63d43-108">Hämta information om identitets leverantörens konfiguration.</span><span class="sxs-lookup"><span data-stu-id="63d43-108">Get the identity provider configuration details.</span></span>

## <span data-ttu-id="63d43-109">BESKRIVS</span><span class="sxs-lookup"><span data-stu-id="63d43-109">EXAMPLES</span></span>

### <span data-ttu-id="63d43-110">Exempel 1: skaffa alla identitets leverantörer</span><span class="sxs-lookup"><span data-stu-id="63d43-110">Example 1: Get all Identity Providers</span></span>

```powershell
PS C:\>$apimContext = New-AzApiManagementContext -ResourceGroupName "Api-Default-WestUS" -ServiceName "contoso"
PS C:\>Get-AzApiManagementIdentityProvider -Context $apimContext
```

<span data-ttu-id="63d43-111">Få all konfigurering av identitetsprovider på tjänsten.</span><span class="sxs-lookup"><span data-stu-id="63d43-111">Get all the identity provider Configuration on the service.</span></span>

### <span data-ttu-id="63d43-112">Exempel 2: Hämta ID för AAD-typ</span><span class="sxs-lookup"><span data-stu-id="63d43-112">Example 2: Get the AAD Type Identity Provider</span></span>
```powershell
PS C:\>$apimContext = New-AzApiManagementContext -ResourceGroupName "Api-Default-WestUS" -ServiceName "contoso"
PS C:\> Get-AzApiManagementIdentityProvider -Context $apimContext -Type Aad


Type                     : Aad
ClientId                 : aaa
ClientSecret             : xxxxx
AllowedTenants           : {contosotest.onmicrosoft.com}
Authority                : login.microsoftonline.com
SignupPolicyName         :
SigninPolicyName         :
ProfileEditingPolicyName :
PasswordResetPolicyName  :
SigninTenant             :
Id                       : /subscriptions/a200340d-6b82-494d-9dbf-687ba6e33f9e/resourceGroups/Api-Default-West-US/providers/Microsoft.ApiManagement/service/contoso/identityProviders/Aad
ResourceGroupName        : Api-Default-West-US
ServiceName              : contoso
```

<span data-ttu-id="63d43-113">Hämtar identitets leverantörs konfigurationen för Azure Active Directory.</span><span class="sxs-lookup"><span data-stu-id="63d43-113">Gets the Identity Provider Configuration of Azure Active Directory.</span></span>

### <span data-ttu-id="63d43-114">Exempel 3: Hämta ID för AAD-B2C</span><span class="sxs-lookup"><span data-stu-id="63d43-114">Example 3: Get the AAD B2C Type Identity Provider</span></span>
```powershell
PS C:\>$context = New-AzApiManagementContext -ResourceGroupName "Api-Default-WestUS" -ServiceName "contoso"
PS C:\> Get-AzApiManagementIdentityProvider -Context $context -Type AadB2C


Type                     : AadB2C
ClientId                 : f02dafe2-b8b8-48ec-a38e-27e5c16c51e5
ClientSecret             : xxxxxx
AllowedTenants           : {contosoaadb2c.onmicrosoft.com}
Authority                : login.microsoftonline.com
SignupPolicyName         : B2C_1_policy-signup
SigninPolicyName         : B2C_1_policy-signin
ProfileEditingPolicyName :
PasswordResetPolicyName  :
SigninTenant             : contosoaadb2c.onmicrosoft.com
Id                       : /subscriptions/a200340d-6b82-494d-9dbf-687ba6e33f9e/resourceGroups/Api-Default-West-US/providers/Microsoft.ApiManagement/service/contoso/identityProviders/AadB2C
ResourceGroupName        : Api-Default-West-US
ServiceName              : contoso
```

<span data-ttu-id="63d43-115">Hämtar identitets leverantörs konfigurationen för Azure Active Directory.</span><span class="sxs-lookup"><span data-stu-id="63d43-115">Gets the Identity Provider Configuration of Azure Active Directory.</span></span>

## <span data-ttu-id="63d43-116">MALLPARAMETRAR</span><span class="sxs-lookup"><span data-stu-id="63d43-116">PARAMETERS</span></span>

### <span data-ttu-id="63d43-117">-Kontext</span><span class="sxs-lookup"><span data-stu-id="63d43-117">-Context</span></span>
<span data-ttu-id="63d43-118">Instans av PsApiManagementContext.</span><span class="sxs-lookup"><span data-stu-id="63d43-118">Instance of PsApiManagementContext.</span></span>
<span data-ttu-id="63d43-119">Denna parameter är obligatorisk.</span><span class="sxs-lookup"><span data-stu-id="63d43-119">This parameter is required.</span></span>

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

### <span data-ttu-id="63d43-120">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="63d43-120">-DefaultProfile</span></span>
<span data-ttu-id="63d43-121">Autentiseringsuppgifter, konto, klient organisation och abonnemang som används för kommunikation med Azure.</span><span class="sxs-lookup"><span data-stu-id="63d43-121">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="63d43-122">– Skriv</span><span class="sxs-lookup"><span data-stu-id="63d43-122">-Type</span></span>
<span data-ttu-id="63d43-123">Identifierare för en identitets leverantör.</span><span class="sxs-lookup"><span data-stu-id="63d43-123">Identifier of a Identity Provider.</span></span>
<span data-ttu-id="63d43-124">Om det här alternativet anges kan du hitta identitets leverantörens konfiguration enligt ID.</span><span class="sxs-lookup"><span data-stu-id="63d43-124">If specified will try to find identity provider configuration by the identifier.</span></span>
<span data-ttu-id="63d43-125">Denna parameter är valfri.</span><span class="sxs-lookup"><span data-stu-id="63d43-125">This parameter is optional.</span></span>

```yaml
Type: Microsoft.Azure.Commands.ApiManagement.ServiceManagement.Models.PsApiManagementIdentityProviderType
Parameter Sets: IdentityProviderByType
Aliases:
Accepted values: Facebook, Google, Microsoft, Twitter, Aad, AadB2C

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="63d43-126">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="63d43-126">CommonParameters</span></span>
<span data-ttu-id="63d43-127">Den här cmdleten har stöd för de gemensamma parametrarna:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-disvariable,-utbuffer,-PipelineVariable,-verbose,-WarningAction och-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="63d43-127">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="63d43-128">Mer information finns i [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="63d43-128">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="63d43-129">KOSTNADS</span><span class="sxs-lookup"><span data-stu-id="63d43-129">INPUTS</span></span>

### <span data-ttu-id="63d43-130">Microsoft. Azure. commands. ApiManagement. ServiceManagement. Models. PsApiManagementContext</span><span class="sxs-lookup"><span data-stu-id="63d43-130">Microsoft.Azure.Commands.ApiManagement.ServiceManagement.Models.PsApiManagementContext</span></span>

### <span data-ttu-id="63d43-131">Microsoft. Azure. commands. ApiManagement. ServiceManagement. Models. PsApiManagementIdentityProviderType</span><span class="sxs-lookup"><span data-stu-id="63d43-131">Microsoft.Azure.Commands.ApiManagement.ServiceManagement.Models.PsApiManagementIdentityProviderType</span></span>

## <span data-ttu-id="63d43-132">VÄRDEN</span><span class="sxs-lookup"><span data-stu-id="63d43-132">OUTPUTS</span></span>

### <span data-ttu-id="63d43-133">Microsoft. Azure. commands. ApiManagement. ServiceManagement. Models. PsApiManagementIdentityProvider</span><span class="sxs-lookup"><span data-stu-id="63d43-133">Microsoft.Azure.Commands.ApiManagement.ServiceManagement.Models.PsApiManagementIdentityProvider</span></span>

## <span data-ttu-id="63d43-134">ANMÄRKNINGAR</span><span class="sxs-lookup"><span data-stu-id="63d43-134">NOTES</span></span>

## <span data-ttu-id="63d43-135">RELATERADE LÄNKAR</span><span class="sxs-lookup"><span data-stu-id="63d43-135">RELATED LINKS</span></span>
