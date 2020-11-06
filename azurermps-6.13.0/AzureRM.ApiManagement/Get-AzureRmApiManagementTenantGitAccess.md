---
external help file: Microsoft.Azure.Commands.ApiManagement.ServiceManagement.dll-Help.xml
Module Name: AzureRM.ApiManagement
ms.assetid: 6F01F494-CD1D-483A-9E57-BF693B1F2FC1
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.apimanagement/get-azurermapimanagementtenantgitaccess
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/ApiManagement/Commands.ApiManagement/help/Get-AzureRmApiManagementTenantGitAccess.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/ApiManagement/Commands.ApiManagement/help/Get-AzureRmApiManagementTenantGitAccess.md
ms.openlocfilehash: 643877de4ab2b9107459beaa7acb276072a249ab
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: sv-SE
ms.lasthandoff: 08/20/2020
ms.locfileid: "93576354"
---
# <span data-ttu-id="1b4d4-101">Get-AzureRmApiManagementTenantGitAccess</span><span class="sxs-lookup"><span data-stu-id="1b4d4-101">Get-AzureRmApiManagementTenantGitAccess</span></span>

## <span data-ttu-id="1b4d4-102">Sammanfattning</span><span class="sxs-lookup"><span data-stu-id="1b4d4-102">SYNOPSIS</span></span>
<span data-ttu-id="1b4d4-103">Hämtar git-åtkomst-konfigurationen för en innehavare.</span><span class="sxs-lookup"><span data-stu-id="1b4d4-103">Gets the Git access configuration for a tenant.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="1b4d4-104">FRÅGESYNTAXEN</span><span class="sxs-lookup"><span data-stu-id="1b4d4-104">SYNTAX</span></span>

```
Get-AzureRmApiManagementTenantGitAccess -Context <PsApiManagementContext>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="1b4d4-105">PROBLEMBESKRIVNING</span><span class="sxs-lookup"><span data-stu-id="1b4d4-105">DESCRIPTION</span></span>
<span data-ttu-id="1b4d4-106">Cmdleten **Get-AzureRmApiManagementTenantGitAccess** hämtar konfigurationen för git-åtkomst för en innehavare.</span><span class="sxs-lookup"><span data-stu-id="1b4d4-106">The **Get-AzureRmApiManagementTenantGitAccess** cmdlet gets the Git access configuration for a tenant.</span></span>

## <span data-ttu-id="1b4d4-107">BESKRIVS</span><span class="sxs-lookup"><span data-stu-id="1b4d4-107">EXAMPLES</span></span>

### <span data-ttu-id="1b4d4-108">Exempel 1: Hämta konfiguration för klient åtkomst</span><span class="sxs-lookup"><span data-stu-id="1b4d4-108">Example 1: Get tenant access configuration</span></span>
```
PS C:\>$apimContext = New-AzureRmApiManagementContext -ResourceGroupName "Api-Default-WestUS" -ServiceName "contoso"
PS C:\>Get-AzureRmApiManagementTenantGitAccess -Context $apimContext
```

<span data-ttu-id="1b4d4-109">Det här kommandot får git-konfigurationen för den angivna kontexten.</span><span class="sxs-lookup"><span data-stu-id="1b4d4-109">This command gets the Git access configuration for the specified context.</span></span>

## <span data-ttu-id="1b4d4-110">MALLPARAMETRAR</span><span class="sxs-lookup"><span data-stu-id="1b4d4-110">PARAMETERS</span></span>

### <span data-ttu-id="1b4d4-111">-Kontext</span><span class="sxs-lookup"><span data-stu-id="1b4d4-111">-Context</span></span>
<span data-ttu-id="1b4d4-112">Anger ett **PsApiManagementContext** -objekt.</span><span class="sxs-lookup"><span data-stu-id="1b4d4-112">Specifies a **PsApiManagementContext** object.</span></span>

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

### <span data-ttu-id="1b4d4-113">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="1b4d4-113">-DefaultProfile</span></span>
<span data-ttu-id="1b4d4-114">Autentiseringsuppgifter, konto, klient organisation och abonnemang som används för kommunikation med Azure.</span><span class="sxs-lookup"><span data-stu-id="1b4d4-114">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="1b4d4-115">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="1b4d4-115">CommonParameters</span></span>
<span data-ttu-id="1b4d4-116">Den här cmdleten har stöd för de gemensamma parametrarna:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-disvariable,-utbuffer,-PipelineVariable,-verbose,-WarningAction och-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="1b4d4-116">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="1b4d4-117">Mer information finns i about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="1b4d4-117">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="1b4d4-118">KOSTNADS</span><span class="sxs-lookup"><span data-stu-id="1b4d4-118">INPUTS</span></span>

### <span data-ttu-id="1b4d4-119">Microsoft. Azure. commands. ApiManagement. ServiceManagement. Models. PsApiManagementContext</span><span class="sxs-lookup"><span data-stu-id="1b4d4-119">Microsoft.Azure.Commands.ApiManagement.ServiceManagement.Models.PsApiManagementContext</span></span>

## <span data-ttu-id="1b4d4-120">VÄRDEN</span><span class="sxs-lookup"><span data-stu-id="1b4d4-120">OUTPUTS</span></span>

### <span data-ttu-id="1b4d4-121">Microsoft. Azure. commands. ApiManagement. ServiceManagement. Models. PsApiManagementAccessInformation</span><span class="sxs-lookup"><span data-stu-id="1b4d4-121">Microsoft.Azure.Commands.ApiManagement.ServiceManagement.Models.PsApiManagementAccessInformation</span></span>

## <span data-ttu-id="1b4d4-122">ANMÄRKNINGAR</span><span class="sxs-lookup"><span data-stu-id="1b4d4-122">NOTES</span></span>

## <span data-ttu-id="1b4d4-123">RELATERADE LÄNKAR</span><span class="sxs-lookup"><span data-stu-id="1b4d4-123">RELATED LINKS</span></span>
