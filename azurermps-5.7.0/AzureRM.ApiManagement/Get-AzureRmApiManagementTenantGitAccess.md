---
external help file: Microsoft.Azure.Commands.ApiManagement.ServiceManagement.dll-Help.xml
ms.assetid: 6F01F494-CD1D-483A-9E57-BF693B1F2FC1
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.apimanagement/get-azurermapimanagementtenantgitaccess
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/ApiManagement/Commands.ApiManagement/help/Get-AzureRmApiManagementTenantGitAccess.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/ApiManagement/Commands.ApiManagement/help/Get-AzureRmApiManagementTenantGitAccess.md
ms.openlocfilehash: 28b27ee7a2e24b425d5ffa93be4d1f3513a31c08
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: sv-SE
ms.lasthandoff: 08/20/2020
ms.locfileid: "93576655"
---
# <span data-ttu-id="91de8-101">Get-AzureRmApiManagementTenantGitAccess</span><span class="sxs-lookup"><span data-stu-id="91de8-101">Get-AzureRmApiManagementTenantGitAccess</span></span>

## <span data-ttu-id="91de8-102">Sammanfattning</span><span class="sxs-lookup"><span data-stu-id="91de8-102">SYNOPSIS</span></span>
<span data-ttu-id="91de8-103">Hämtar git-åtkomst-konfigurationen för en innehavare.</span><span class="sxs-lookup"><span data-stu-id="91de8-103">Gets the Git access configuration for a tenant.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="91de8-104">FRÅGESYNTAXEN</span><span class="sxs-lookup"><span data-stu-id="91de8-104">SYNTAX</span></span>

```
Get-AzureRmApiManagementTenantGitAccess -Context <PsApiManagementContext>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="91de8-105">PROBLEMBESKRIVNING</span><span class="sxs-lookup"><span data-stu-id="91de8-105">DESCRIPTION</span></span>
<span data-ttu-id="91de8-106">Cmdleten **Get-AzureRmApiManagementTenantGitAccess** hämtar konfigurationen för git-åtkomst för en innehavare.</span><span class="sxs-lookup"><span data-stu-id="91de8-106">The **Get-AzureRmApiManagementTenantGitAccess** cmdlet gets the Git access configuration for a tenant.</span></span>

## <span data-ttu-id="91de8-107">BESKRIVS</span><span class="sxs-lookup"><span data-stu-id="91de8-107">EXAMPLES</span></span>

### <span data-ttu-id="91de8-108">Exempel 1: Hämta konfiguration för klient åtkomst</span><span class="sxs-lookup"><span data-stu-id="91de8-108">Example 1: Get tenant access configuration</span></span>
```
PS C:\>$apimContext = New-AzureRmApiManagementContext -ResourceGroupName "Api-Default-WestUS" -ServiceName "contoso"
PS C:\>Get-AzureRmApiManagementTenantGitAccess -Context $apimContext 
```

<span data-ttu-id="91de8-109">Det här kommandot får git-konfigurationen för den angivna kontexten.</span><span class="sxs-lookup"><span data-stu-id="91de8-109">This command gets the Git access configuration for the specified context.</span></span>

## <span data-ttu-id="91de8-110">MALLPARAMETRAR</span><span class="sxs-lookup"><span data-stu-id="91de8-110">PARAMETERS</span></span>

### <span data-ttu-id="91de8-111">-Kontext</span><span class="sxs-lookup"><span data-stu-id="91de8-111">-Context</span></span>
<span data-ttu-id="91de8-112">Anger ett **PsApiManagementContext** -objekt.</span><span class="sxs-lookup"><span data-stu-id="91de8-112">Specifies a **PsApiManagementContext** object.</span></span>

```yaml
Type: PsApiManagementContext
Parameter Sets: (All)
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="91de8-113">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="91de8-113">-DefaultProfile</span></span>
<span data-ttu-id="91de8-114">Autentiseringsuppgifter, konto, klient organisation och abonnemang som används för kommunikation med Azure.</span><span class="sxs-lookup"><span data-stu-id="91de8-114">The credentials, account, tenant, and subscription used for communication with azure.</span></span>
 
```yaml
Type: IAzureContextContainer
Parameter Sets: (All)
Aliases: AzureRmContext, AzureCredential

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="91de8-115">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="91de8-115">CommonParameters</span></span>
<span data-ttu-id="91de8-116">Den här cmdleten har stöd för de gemensamma parametrarna:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-disvariable,-utbuffer,-PipelineVariable,-verbose,-WarningAction och-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="91de8-116">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="91de8-117">Mer information finns i about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="91de8-117">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="91de8-118">KOSTNADS</span><span class="sxs-lookup"><span data-stu-id="91de8-118">INPUTS</span></span>

### <span data-ttu-id="91de8-119">Ingen</span><span class="sxs-lookup"><span data-stu-id="91de8-119">None</span></span>
<span data-ttu-id="91de8-120">Denna cmdlet accepterar inte indata.</span><span class="sxs-lookup"><span data-stu-id="91de8-120">This cmdlet does not accept any input.</span></span>

## <span data-ttu-id="91de8-121">VÄRDEN</span><span class="sxs-lookup"><span data-stu-id="91de8-121">OUTPUTS</span></span>

### <span data-ttu-id="91de8-122">Microsoft. Azure. commands. ApiManagement. ServiceManagement. Models. PsApiManagementAccessInformation</span><span class="sxs-lookup"><span data-stu-id="91de8-122">Microsoft.Azure.Commands.ApiManagement.ServiceManagement.Models.PsApiManagementAccessInformation</span></span>

## <span data-ttu-id="91de8-123">ANMÄRKNINGAR</span><span class="sxs-lookup"><span data-stu-id="91de8-123">NOTES</span></span>

## <span data-ttu-id="91de8-124">RELATERADE LÄNKAR</span><span class="sxs-lookup"><span data-stu-id="91de8-124">RELATED LINKS</span></span>

