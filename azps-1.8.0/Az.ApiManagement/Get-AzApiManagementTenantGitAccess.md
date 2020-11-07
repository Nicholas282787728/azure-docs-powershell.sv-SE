---
external help file: Microsoft.Azure.PowerShell.Cmdlets.ApiManagement.ServiceManagement.dll-Help.xml
Module Name: Az.ApiManagement
ms.assetid: 6F01F494-CD1D-483A-9E57-BF693B1F2FC1
online version: https://docs.microsoft.com/en-us/powershell/module/az.apimanagement/get-azapimanagementtenantgitaccess
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/ApiManagement/ApiManagement/help/Get-AzApiManagementTenantGitAccess.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/ApiManagement/ApiManagement/help/Get-AzApiManagementTenantGitAccess.md
ms.openlocfilehash: 2fe14349b179634bf93050840271d4d4b6905b3f
ms.sourcegitcommit: 4d2c178cd6df9151877b08d54c1f4a228dbec9d1
ms.translationtype: MT
ms.contentlocale: sv-SE
ms.lasthandoff: 01/29/2020
ms.locfileid: "93743390"
---
# <span data-ttu-id="029d5-101">Get-AzApiManagementTenantGitAccess</span><span class="sxs-lookup"><span data-stu-id="029d5-101">Get-AzApiManagementTenantGitAccess</span></span>

## <span data-ttu-id="029d5-102">Sammanfattning</span><span class="sxs-lookup"><span data-stu-id="029d5-102">SYNOPSIS</span></span>
<span data-ttu-id="029d5-103">Hämtar git-åtkomst-konfigurationen för en innehavare.</span><span class="sxs-lookup"><span data-stu-id="029d5-103">Gets the Git access configuration for a tenant.</span></span>

## <span data-ttu-id="029d5-104">FRÅGESYNTAXEN</span><span class="sxs-lookup"><span data-stu-id="029d5-104">SYNTAX</span></span>

```
Get-AzApiManagementTenantGitAccess -Context <PsApiManagementContext> [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

## <span data-ttu-id="029d5-105">PROBLEMBESKRIVNING</span><span class="sxs-lookup"><span data-stu-id="029d5-105">DESCRIPTION</span></span>
<span data-ttu-id="029d5-106">Cmdleten **Get-AzApiManagementTenantGitAccess** hämtar konfigurationen för git-åtkomst för en innehavare.</span><span class="sxs-lookup"><span data-stu-id="029d5-106">The **Get-AzApiManagementTenantGitAccess** cmdlet gets the Git access configuration for a tenant.</span></span>

## <span data-ttu-id="029d5-107">BESKRIVS</span><span class="sxs-lookup"><span data-stu-id="029d5-107">EXAMPLES</span></span>

### <span data-ttu-id="029d5-108">Exempel 1: Hämta konfiguration för klient åtkomst</span><span class="sxs-lookup"><span data-stu-id="029d5-108">Example 1: Get tenant access configuration</span></span>
```
PS C:\>$apimContext = New-AzApiManagementContext -ResourceGroupName "Api-Default-WestUS" -ServiceName "contoso"
PS C:\>Get-AzApiManagementTenantGitAccess -Context $apimContext
```

<span data-ttu-id="029d5-109">Det här kommandot får git-konfigurationen för den angivna kontexten.</span><span class="sxs-lookup"><span data-stu-id="029d5-109">This command gets the Git access configuration for the specified context.</span></span>

## <span data-ttu-id="029d5-110">MALLPARAMETRAR</span><span class="sxs-lookup"><span data-stu-id="029d5-110">PARAMETERS</span></span>

### <span data-ttu-id="029d5-111">-Kontext</span><span class="sxs-lookup"><span data-stu-id="029d5-111">-Context</span></span>
<span data-ttu-id="029d5-112">Anger ett **PsApiManagementContext** -objekt.</span><span class="sxs-lookup"><span data-stu-id="029d5-112">Specifies a **PsApiManagementContext** object.</span></span>

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

### <span data-ttu-id="029d5-113">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="029d5-113">-DefaultProfile</span></span>
<span data-ttu-id="029d5-114">Autentiseringsuppgifter, konto, klient organisation och abonnemang som används för kommunikation med Azure.</span><span class="sxs-lookup"><span data-stu-id="029d5-114">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="029d5-115">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="029d5-115">CommonParameters</span></span>
<span data-ttu-id="029d5-116">Den här cmdleten har stöd för de gemensamma parametrarna:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-disvariable,-utbuffer,-PipelineVariable,-verbose,-WarningAction och-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="029d5-116">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="029d5-117">Mer information finns i about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="029d5-117">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="029d5-118">KOSTNADS</span><span class="sxs-lookup"><span data-stu-id="029d5-118">INPUTS</span></span>

### <span data-ttu-id="029d5-119">Microsoft. Azure. commands. ApiManagement. ServiceManagement. Models. PsApiManagementContext</span><span class="sxs-lookup"><span data-stu-id="029d5-119">Microsoft.Azure.Commands.ApiManagement.ServiceManagement.Models.PsApiManagementContext</span></span>

## <span data-ttu-id="029d5-120">VÄRDEN</span><span class="sxs-lookup"><span data-stu-id="029d5-120">OUTPUTS</span></span>

### <span data-ttu-id="029d5-121">Microsoft. Azure. commands. ApiManagement. ServiceManagement. Models. PsApiManagementAccessInformation</span><span class="sxs-lookup"><span data-stu-id="029d5-121">Microsoft.Azure.Commands.ApiManagement.ServiceManagement.Models.PsApiManagementAccessInformation</span></span>

## <span data-ttu-id="029d5-122">ANMÄRKNINGAR</span><span class="sxs-lookup"><span data-stu-id="029d5-122">NOTES</span></span>

## <span data-ttu-id="029d5-123">RELATERADE LÄNKAR</span><span class="sxs-lookup"><span data-stu-id="029d5-123">RELATED LINKS</span></span>
