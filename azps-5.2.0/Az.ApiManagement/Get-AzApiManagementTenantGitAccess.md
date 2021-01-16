---
external help file: Microsoft.Azure.PowerShell.Cmdlets.ApiManagement.ServiceManagement.dll-Help.xml
Module Name: Az.ApiManagement
ms.assetid: 6F01F494-CD1D-483A-9E57-BF693B1F2FC1
online version: https://docs.microsoft.com/en-us/powershell/module/az.apimanagement/get-azapimanagementtenantgitaccess
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/ApiManagement/ApiManagement/help/Get-AzApiManagementTenantGitAccess.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/ApiManagement/ApiManagement/help/Get-AzApiManagementTenantGitAccess.md
ms.openlocfilehash: 0a3d2aeb8c90377f9c7e81ef6a25cef49780e410
ms.sourcegitcommit: 04221336bc9eed46c05ed1e828a6811534d4b4ab
ms.translationtype: MT
ms.contentlocale: sv-SE
ms.lasthandoff: 12/08/2020
ms.locfileid: "98391771"
---
# <span data-ttu-id="30c8f-101">Get-AzApiManagementTenantGitAccess</span><span class="sxs-lookup"><span data-stu-id="30c8f-101">Get-AzApiManagementTenantGitAccess</span></span>

## <span data-ttu-id="30c8f-102">Sammanfattning</span><span class="sxs-lookup"><span data-stu-id="30c8f-102">SYNOPSIS</span></span>
<span data-ttu-id="30c8f-103">Hämtar git-åtkomst-konfigurationen för en innehavare.</span><span class="sxs-lookup"><span data-stu-id="30c8f-103">Gets the Git access configuration for a tenant.</span></span>

## <span data-ttu-id="30c8f-104">FRÅGESYNTAXEN</span><span class="sxs-lookup"><span data-stu-id="30c8f-104">SYNTAX</span></span>

```
Get-AzApiManagementTenantGitAccess -Context <PsApiManagementContext> [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

## <span data-ttu-id="30c8f-105">PROBLEMBESKRIVNING</span><span class="sxs-lookup"><span data-stu-id="30c8f-105">DESCRIPTION</span></span>
<span data-ttu-id="30c8f-106">Cmdleten **Get-AzApiManagementTenantGitAccess** hämtar konfigurationen för git-åtkomst för en innehavare.</span><span class="sxs-lookup"><span data-stu-id="30c8f-106">The **Get-AzApiManagementTenantGitAccess** cmdlet gets the Git access configuration for a tenant.</span></span>
<span data-ttu-id="30c8f-107">Nycklarna tas inte med i resultatet.</span><span class="sxs-lookup"><span data-stu-id="30c8f-107">Keys will not be included into result details.</span></span> <span data-ttu-id="30c8f-108">Använd **Get-AzApiManagementTenantGitAccessSecret** för att få klient hemlighet.</span><span class="sxs-lookup"><span data-stu-id="30c8f-108">To get client secret, use **Get-AzApiManagementTenantGitAccessSecret**.</span></span>

## <span data-ttu-id="30c8f-109">BESKRIVS</span><span class="sxs-lookup"><span data-stu-id="30c8f-109">EXAMPLES</span></span>

### <span data-ttu-id="30c8f-110">Exempel 1: Hämta konfiguration för klient åtkomst</span><span class="sxs-lookup"><span data-stu-id="30c8f-110">Example 1: Get tenant access configuration</span></span>
```powershell
PS C:\>$apimContext = New-AzApiManagementContext -ResourceGroupName "Api-Default-WestUS" -ServiceName "contoso"
PS C:\>Get-AzApiManagementTenantGitAccess -Context $apimContext
```

```
Enabled Id  PrimaryKey                                                                               SecondaryKey
------- --  ----------                                                                               ------------
   True git GrPksEiunqn1BgprRvWIZZxUuaRl9vdz0ZFjVBxxx==             OR4wVD//HzaE4Okb6aSdG9zy0O6kHhmfIJBaL9Zwu+Mxxxf9R2ydOslIw==
```

<span data-ttu-id="30c8f-111">Det här kommandot får git-konfigurationen för den angivna kontexten.</span><span class="sxs-lookup"><span data-stu-id="30c8f-111">This command gets the Git access configuration for the specified context.</span></span>

## <span data-ttu-id="30c8f-112">MALLPARAMETRAR</span><span class="sxs-lookup"><span data-stu-id="30c8f-112">PARAMETERS</span></span>

### <span data-ttu-id="30c8f-113">-Kontext</span><span class="sxs-lookup"><span data-stu-id="30c8f-113">-Context</span></span>
<span data-ttu-id="30c8f-114">Anger ett **PsApiManagementContext** -objekt.</span><span class="sxs-lookup"><span data-stu-id="30c8f-114">Specifies a **PsApiManagementContext** object.</span></span>

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

### <span data-ttu-id="30c8f-115">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="30c8f-115">-DefaultProfile</span></span>
<span data-ttu-id="30c8f-116">Autentiseringsuppgifter, konto, klient organisation och abonnemang som används för kommunikation med Azure.</span><span class="sxs-lookup"><span data-stu-id="30c8f-116">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="30c8f-117">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="30c8f-117">CommonParameters</span></span>
<span data-ttu-id="30c8f-118">Den här cmdleten har stöd för de gemensamma parametrarna:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-disvariable,-utbuffer,-PipelineVariable,-verbose,-WarningAction och-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="30c8f-118">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="30c8f-119">Mer information finns i [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="30c8f-119">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="30c8f-120">KOSTNADS</span><span class="sxs-lookup"><span data-stu-id="30c8f-120">INPUTS</span></span>

### <span data-ttu-id="30c8f-121">Microsoft. Azure. commands. ApiManagement. ServiceManagement. Models. PsApiManagementContext</span><span class="sxs-lookup"><span data-stu-id="30c8f-121">Microsoft.Azure.Commands.ApiManagement.ServiceManagement.Models.PsApiManagementContext</span></span>

## <span data-ttu-id="30c8f-122">VÄRDEN</span><span class="sxs-lookup"><span data-stu-id="30c8f-122">OUTPUTS</span></span>

### <span data-ttu-id="30c8f-123">Microsoft. Azure. commands. ApiManagement. ServiceManagement. Models. PsApiManagementAccessInformation</span><span class="sxs-lookup"><span data-stu-id="30c8f-123">Microsoft.Azure.Commands.ApiManagement.ServiceManagement.Models.PsApiManagementAccessInformation</span></span>

## <span data-ttu-id="30c8f-124">ANMÄRKNINGAR</span><span class="sxs-lookup"><span data-stu-id="30c8f-124">NOTES</span></span>

## <span data-ttu-id="30c8f-125">RELATERADE LÄNKAR</span><span class="sxs-lookup"><span data-stu-id="30c8f-125">RELATED LINKS</span></span>
