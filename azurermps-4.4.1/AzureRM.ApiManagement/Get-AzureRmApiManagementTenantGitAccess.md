---
external help file: Microsoft.Azure.Commands.ApiManagement.ServiceManagement.dll-Help.xml
Module Name: AzureRM.ApiManagement
ms.assetid: 6F01F494-CD1D-483A-9E57-BF693B1F2FC1
online version: ''
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/ApiManagement/Commands.ApiManagement/help/Get-AzureRmApiManagementTenantGitAccess.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/ApiManagement/Commands.ApiManagement/help/Get-AzureRmApiManagementTenantGitAccess.md
ms.openlocfilehash: 69f643f4d2e66f0b5af61a6362e59386b2f79078
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: sv-SE
ms.lasthandoff: 08/20/2020
ms.locfileid: "93583891"
---
# <span data-ttu-id="0b840-101">Get-AzureRmApiManagementTenantGitAccess</span><span class="sxs-lookup"><span data-stu-id="0b840-101">Get-AzureRmApiManagementTenantGitAccess</span></span>

## <span data-ttu-id="0b840-102">Sammanfattning</span><span class="sxs-lookup"><span data-stu-id="0b840-102">SYNOPSIS</span></span>
<span data-ttu-id="0b840-103">Hämtar git-åtkomst-konfigurationen för en innehavare.</span><span class="sxs-lookup"><span data-stu-id="0b840-103">Gets the Git access configuration for a tenant.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="0b840-104">FRÅGESYNTAXEN</span><span class="sxs-lookup"><span data-stu-id="0b840-104">SYNTAX</span></span>

```
Get-AzureRmApiManagementTenantGitAccess -Context <PsApiManagementContext>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="0b840-105">PROBLEMBESKRIVNING</span><span class="sxs-lookup"><span data-stu-id="0b840-105">DESCRIPTION</span></span>
<span data-ttu-id="0b840-106">Cmdleten **Get-AzureRmApiManagementTenantGitAccess** hämtar konfigurationen för git-åtkomst för en innehavare.</span><span class="sxs-lookup"><span data-stu-id="0b840-106">The **Get-AzureRmApiManagementTenantGitAccess** cmdlet gets the Git access configuration for a tenant.</span></span>

## <span data-ttu-id="0b840-107">BESKRIVS</span><span class="sxs-lookup"><span data-stu-id="0b840-107">EXAMPLES</span></span>

### <span data-ttu-id="0b840-108">Exempel 1: Hämta konfiguration för klient åtkomst</span><span class="sxs-lookup"><span data-stu-id="0b840-108">Example 1: Get tenant access configuration</span></span>
```
PS C:\>Get-AzureRmApiManagementTenantGitAccess -Context $ApimContext
```

<span data-ttu-id="0b840-109">Det här kommandot får git-konfigurationen för den angivna kontexten.</span><span class="sxs-lookup"><span data-stu-id="0b840-109">This command gets the Git access configuration for the specified context.</span></span>

## <span data-ttu-id="0b840-110">MALLPARAMETRAR</span><span class="sxs-lookup"><span data-stu-id="0b840-110">PARAMETERS</span></span>

### <span data-ttu-id="0b840-111">-Kontext</span><span class="sxs-lookup"><span data-stu-id="0b840-111">-Context</span></span>
<span data-ttu-id="0b840-112">Anger ett **PsApiManagementContext** -objekt.</span><span class="sxs-lookup"><span data-stu-id="0b840-112">Specifies a **PsApiManagementContext** object.</span></span>

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

### <span data-ttu-id="0b840-113">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="0b840-113">-DefaultProfile</span></span>
<span data-ttu-id="0b840-114">Autentiseringsuppgifter, konto, klient organisation och abonnemang som används för kommunikation med Azure.</span><span class="sxs-lookup"><span data-stu-id="0b840-114">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="0b840-115">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="0b840-115">CommonParameters</span></span>
<span data-ttu-id="0b840-116">Den här cmdleten har stöd för de gemensamma parametrarna:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-disvariable,-utbuffer,-PipelineVariable,-verbose,-WarningAction och-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="0b840-116">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="0b840-117">Mer information finns i about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="0b840-117">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="0b840-118">KOSTNADS</span><span class="sxs-lookup"><span data-stu-id="0b840-118">INPUTS</span></span>

## <span data-ttu-id="0b840-119">VÄRDEN</span><span class="sxs-lookup"><span data-stu-id="0b840-119">OUTPUTS</span></span>

### <span data-ttu-id="0b840-120">Microsoft. Azure. commands. ApiManagement. ServiceManagement. Models. PsApiManagementAccessInformation</span><span class="sxs-lookup"><span data-stu-id="0b840-120">Microsoft.Azure.Commands.ApiManagement.ServiceManagement.Models.PsApiManagementAccessInformation</span></span>

## <span data-ttu-id="0b840-121">ANMÄRKNINGAR</span><span class="sxs-lookup"><span data-stu-id="0b840-121">NOTES</span></span>

## <span data-ttu-id="0b840-122">RELATERADE LÄNKAR</span><span class="sxs-lookup"><span data-stu-id="0b840-122">RELATED LINKS</span></span>

