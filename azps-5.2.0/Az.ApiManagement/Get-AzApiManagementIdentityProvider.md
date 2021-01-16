---
external help file: Microsoft.Azure.PowerShell.Cmdlets.ApiManagement.ServiceManagement.dll-Help.xml
Module Name: Az.ApiManagement
online version: https://docs.microsoft.com/en-us/powershell/module/az.apimanagement/get-azapimanagementidentityprovider
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/ApiManagement/ApiManagement/help/Get-AzApiManagementIdentityProvider.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/ApiManagement/ApiManagement/help/Get-AzApiManagementIdentityProvider.md
ms.openlocfilehash: b267fc854127c1cb098481ac483a7572c8b2e12f
ms.sourcegitcommit: 04221336bc9eed46c05ed1e828a6811534d4b4ab
ms.translationtype: MT
ms.contentlocale: sv-SE
ms.lasthandoff: 12/08/2020
ms.locfileid: "98387855"
---
# <span data-ttu-id="864fe-101">Get-AzApiManagementIdentityProvider</span><span class="sxs-lookup"><span data-stu-id="864fe-101">Get-AzApiManagementIdentityProvider</span></span>

## <span data-ttu-id="864fe-102">Sammanfattning</span><span class="sxs-lookup"><span data-stu-id="864fe-102">SYNOPSIS</span></span>
<span data-ttu-id="864fe-103">Hämta information om identitets leverantörens konfiguration.</span><span class="sxs-lookup"><span data-stu-id="864fe-103">Get the identity provider configuration details.</span></span>

## <span data-ttu-id="864fe-104">FRÅGESYNTAXEN</span><span class="sxs-lookup"><span data-stu-id="864fe-104">SYNTAX</span></span>

### <span data-ttu-id="864fe-105">AllIdentityProviders (standard)</span><span class="sxs-lookup"><span data-stu-id="864fe-105">AllIdentityProviders (Default)</span></span>
```
Get-AzApiManagementIdentityProvider -Context <PsApiManagementContext>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="864fe-106">IdentityProviderByType</span><span class="sxs-lookup"><span data-stu-id="864fe-106">IdentityProviderByType</span></span>
```
Get-AzApiManagementIdentityProvider -Context <PsApiManagementContext>
 -Type <PsApiManagementIdentityProviderType> [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="864fe-107">PROBLEMBESKRIVNING</span><span class="sxs-lookup"><span data-stu-id="864fe-107">DESCRIPTION</span></span>
<span data-ttu-id="864fe-108">Hämta information om identitets leverantörens konfiguration.</span><span class="sxs-lookup"><span data-stu-id="864fe-108">Get the identity provider configuration details.</span></span>
<span data-ttu-id="864fe-109">ClientSecret tas inte med i resultatet.</span><span class="sxs-lookup"><span data-stu-id="864fe-109">ClientSecret will not be included into result details.</span></span> <span data-ttu-id="864fe-110">Använd **Get-AzApiManagementIdentityProviderClientSecret** för att få klient hemlighet.</span><span class="sxs-lookup"><span data-stu-id="864fe-110">To get client secret, use **Get-AzApiManagementIdentityProviderClientSecret**.</span></span>

## <span data-ttu-id="864fe-111">BESKRIVS</span><span class="sxs-lookup"><span data-stu-id="864fe-111">EXAMPLES</span></span>

### <span data-ttu-id="864fe-112">Exempel 1: skaffa alla identitets leverantörer</span><span class="sxs-lookup"><span data-stu-id="864fe-112">Example 1: Get all Identity Providers</span></span>

```powershell
PS C:\>$apimContext = New-AzApiManagementContext -ResourceGroupName "Api-Default-WestUS" -ServiceName "contoso"
PS C:\>Get-AzApiManagementIdentityProvider -Context $apimContext
```

<span data-ttu-id="864fe-113">Få all konfigurering av identitetsprovider på tjänsten.</span><span class="sxs-lookup"><span data-stu-id="864fe-113">Get all the identity provider Configuration on the service.</span></span>

### <span data-ttu-id="864fe-114">Exempel 2: Hämta ID för AAD-typ</span><span class="sxs-lookup"><span data-stu-id="864fe-114">Example 2: Get the AAD Type Identity Provider</span></span>
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

<span data-ttu-id="864fe-115">Hämtar identitets leverantörs konfigurationen för Azure Active Directory.</span><span class="sxs-lookup"><span data-stu-id="864fe-115">Gets the Identity Provider Configuration of Azure Active Directory.</span></span>

### <span data-ttu-id="864fe-116">Exempel 3: Hämta ID för AAD-B2C</span><span class="sxs-lookup"><span data-stu-id="864fe-116">Example 3: Get the AAD B2C Type Identity Provider</span></span>
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

<span data-ttu-id="864fe-117">Hämtar identitets leverantörs konfigurationen för Azure Active Directory.</span><span class="sxs-lookup"><span data-stu-id="864fe-117">Gets the Identity Provider Configuration of Azure Active Directory.</span></span>

## <span data-ttu-id="864fe-118">MALLPARAMETRAR</span><span class="sxs-lookup"><span data-stu-id="864fe-118">PARAMETERS</span></span>

### <span data-ttu-id="864fe-119">-Kontext</span><span class="sxs-lookup"><span data-stu-id="864fe-119">-Context</span></span>
<span data-ttu-id="864fe-120">Instans av PsApiManagementContext.</span><span class="sxs-lookup"><span data-stu-id="864fe-120">Instance of PsApiManagementContext.</span></span>
<span data-ttu-id="864fe-121">Denna parameter är obligatorisk.</span><span class="sxs-lookup"><span data-stu-id="864fe-121">This parameter is required.</span></span>

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

### <span data-ttu-id="864fe-122">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="864fe-122">-DefaultProfile</span></span>
<span data-ttu-id="864fe-123">Autentiseringsuppgifter, konto, klient organisation och abonnemang som används för kommunikation med Azure.</span><span class="sxs-lookup"><span data-stu-id="864fe-123">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="864fe-124">– Skriv</span><span class="sxs-lookup"><span data-stu-id="864fe-124">-Type</span></span>
<span data-ttu-id="864fe-125">Identifierare för en identitets leverantör.</span><span class="sxs-lookup"><span data-stu-id="864fe-125">Identifier of a Identity Provider.</span></span>
<span data-ttu-id="864fe-126">Om det här alternativet anges kan du hitta identitets leverantörens konfiguration enligt ID.</span><span class="sxs-lookup"><span data-stu-id="864fe-126">If specified will try to find identity provider configuration by the identifier.</span></span>
<span data-ttu-id="864fe-127">Denna parameter är valfri.</span><span class="sxs-lookup"><span data-stu-id="864fe-127">This parameter is optional.</span></span>

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

### <span data-ttu-id="864fe-128">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="864fe-128">CommonParameters</span></span>
<span data-ttu-id="864fe-129">Den här cmdleten har stöd för de gemensamma parametrarna:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-disvariable,-utbuffer,-PipelineVariable,-verbose,-WarningAction och-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="864fe-129">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="864fe-130">Mer information finns i [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="864fe-130">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="864fe-131">KOSTNADS</span><span class="sxs-lookup"><span data-stu-id="864fe-131">INPUTS</span></span>

### <span data-ttu-id="864fe-132">Microsoft. Azure. commands. ApiManagement. ServiceManagement. Models. PsApiManagementContext</span><span class="sxs-lookup"><span data-stu-id="864fe-132">Microsoft.Azure.Commands.ApiManagement.ServiceManagement.Models.PsApiManagementContext</span></span>

### <span data-ttu-id="864fe-133">Microsoft. Azure. commands. ApiManagement. ServiceManagement. Models. PsApiManagementIdentityProviderType</span><span class="sxs-lookup"><span data-stu-id="864fe-133">Microsoft.Azure.Commands.ApiManagement.ServiceManagement.Models.PsApiManagementIdentityProviderType</span></span>

## <span data-ttu-id="864fe-134">VÄRDEN</span><span class="sxs-lookup"><span data-stu-id="864fe-134">OUTPUTS</span></span>

### <span data-ttu-id="864fe-135">Microsoft. Azure. commands. ApiManagement. ServiceManagement. Models. PsApiManagementIdentityProvider</span><span class="sxs-lookup"><span data-stu-id="864fe-135">Microsoft.Azure.Commands.ApiManagement.ServiceManagement.Models.PsApiManagementIdentityProvider</span></span>

## <span data-ttu-id="864fe-136">ANMÄRKNINGAR</span><span class="sxs-lookup"><span data-stu-id="864fe-136">NOTES</span></span>

## <span data-ttu-id="864fe-137">RELATERADE LÄNKAR</span><span class="sxs-lookup"><span data-stu-id="864fe-137">RELATED LINKS</span></span>
