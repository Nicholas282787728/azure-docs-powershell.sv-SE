---
external help file: Microsoft.Azure.Commands.ApiManagement.ServiceManagement.dll-Help.xml
Module Name: AzureRM.ApiManagement
ms.assetid: 236B4436-E8AD-42B4-922C-E2E1406CAFC2
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.apimanagement/get-azurermapimanagementtenantaccess
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/ApiManagement/Commands.ApiManagement/help/Get-AzureRmApiManagementTenantAccess.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/ApiManagement/Commands.ApiManagement/help/Get-AzureRmApiManagementTenantAccess.md
ms.openlocfilehash: 010e52d7c2d05977c8125d5d78d69ef8ac7f75fe
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: sv-SE
ms.lasthandoff: 08/20/2020
ms.locfileid: "93755226"
---
# <span data-ttu-id="631da-101">Get-AzureRmApiManagementTenantAccess</span><span class="sxs-lookup"><span data-stu-id="631da-101">Get-AzureRmApiManagementTenantAccess</span></span>

## <span data-ttu-id="631da-102">Sammanfattning</span><span class="sxs-lookup"><span data-stu-id="631da-102">SYNOPSIS</span></span>
<span data-ttu-id="631da-103">Hämtar åtkomst konfigurationen för en klient organisation.</span><span class="sxs-lookup"><span data-stu-id="631da-103">Gets the access configuration for a tenant.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="631da-104">FRÅGESYNTAXEN</span><span class="sxs-lookup"><span data-stu-id="631da-104">SYNTAX</span></span>

```
Get-AzureRmApiManagementTenantAccess -Context <PsApiManagementContext>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="631da-105">PROBLEMBESKRIVNING</span><span class="sxs-lookup"><span data-stu-id="631da-105">DESCRIPTION</span></span>
<span data-ttu-id="631da-106">Cmdleten **Get-AzureRmApiManagementTenantAccess** hämtar klient åtkomst konfigurationen för en klient organisation.</span><span class="sxs-lookup"><span data-stu-id="631da-106">The **Get-AzureRmApiManagementTenantAccess** cmdlet gets the tenant access configuration for a tenant.</span></span>

## <span data-ttu-id="631da-107">BESKRIVS</span><span class="sxs-lookup"><span data-stu-id="631da-107">EXAMPLES</span></span>

### <span data-ttu-id="631da-108">Exempel 1: Hämta konfiguration för klient åtkomst</span><span class="sxs-lookup"><span data-stu-id="631da-108">Example 1: Get tenant access configuration</span></span>
```
PS C:\>$apimContext = New-AzureRmApiManagementContext -ResourceGroupName "Api-Default-WestUS" -ServiceName "contoso"
PS C:\>Get-AzureRmApiManagementTenantAccess -Context $apimContext
```

<span data-ttu-id="631da-109">Det här kommandot får klient åtkomst konfigurationen för angiven kontext.</span><span class="sxs-lookup"><span data-stu-id="631da-109">This command gets the tenant access configuration for the specified context.</span></span>

## <span data-ttu-id="631da-110">MALLPARAMETRAR</span><span class="sxs-lookup"><span data-stu-id="631da-110">PARAMETERS</span></span>

### <span data-ttu-id="631da-111">-Kontext</span><span class="sxs-lookup"><span data-stu-id="631da-111">-Context</span></span>
<span data-ttu-id="631da-112">Anger ett **PsApiManagementContext** -objekt.</span><span class="sxs-lookup"><span data-stu-id="631da-112">Specifies a **PsApiManagementContext** object.</span></span>

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

### <span data-ttu-id="631da-113">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="631da-113">-DefaultProfile</span></span>
<span data-ttu-id="631da-114">Autentiseringsuppgifter, konto, klient organisation och abonnemang som används för kommunikation med Azure.</span><span class="sxs-lookup"><span data-stu-id="631da-114">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="631da-115">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="631da-115">CommonParameters</span></span>
<span data-ttu-id="631da-116">Den här cmdleten har stöd för de gemensamma parametrarna:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-disvariable,-utbuffer,-PipelineVariable,-verbose,-WarningAction och-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="631da-116">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="631da-117">Mer information finns i about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="631da-117">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="631da-118">KOSTNADS</span><span class="sxs-lookup"><span data-stu-id="631da-118">INPUTS</span></span>

### <span data-ttu-id="631da-119">Microsoft. Azure. commands. ApiManagement. ServiceManagement. Models. PsApiManagementContext</span><span class="sxs-lookup"><span data-stu-id="631da-119">Microsoft.Azure.Commands.ApiManagement.ServiceManagement.Models.PsApiManagementContext</span></span>

## <span data-ttu-id="631da-120">VÄRDEN</span><span class="sxs-lookup"><span data-stu-id="631da-120">OUTPUTS</span></span>

### <span data-ttu-id="631da-121">Microsoft. Azure. commands. ApiManagement. ServiceManagement. Models. PsApiManagementAccessInformation</span><span class="sxs-lookup"><span data-stu-id="631da-121">Microsoft.Azure.Commands.ApiManagement.ServiceManagement.Models.PsApiManagementAccessInformation</span></span>

## <span data-ttu-id="631da-122">ANMÄRKNINGAR</span><span class="sxs-lookup"><span data-stu-id="631da-122">NOTES</span></span>

## <span data-ttu-id="631da-123">RELATERADE LÄNKAR</span><span class="sxs-lookup"><span data-stu-id="631da-123">RELATED LINKS</span></span>

[<span data-ttu-id="631da-124">Set-AzureRmApiManagementTenantAccess</span><span class="sxs-lookup"><span data-stu-id="631da-124">Set-AzureRmApiManagementTenantAccess</span></span>](./Set-AzureRmApiManagementTenantAccess.md)


