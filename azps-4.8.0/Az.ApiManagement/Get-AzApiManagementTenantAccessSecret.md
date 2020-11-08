---
external help file: Microsoft.Azure.PowerShell.Cmdlets.ApiManagement.ServiceManagement.dll-Help.xml
Module Name: Az.ApiManagement
online version: https://docs.microsoft.com/en-us/powershell/module/az.apimanagement/get-azapimanagementtenantaccesssecret
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/ApiManagement/ApiManagement/help/Get-AzApiManagementTenantAccessSecret.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/ApiManagement/ApiManagement/help/Get-AzApiManagementTenantAccessSecret.md
ms.openlocfilehash: ec64a339c29facdbb940b8141c72222ff932c1bd
ms.sourcegitcommit: 1de2b6c3c99197958fa2101bc37680e7507f91ac
ms.translationtype: MT
ms.contentlocale: sv-SE
ms.lasthandoff: 10/13/2020
ms.locfileid: "94102487"
---
# <span data-ttu-id="51469-101">Get-AzApiManagementTenantAccessSecret</span><span class="sxs-lookup"><span data-stu-id="51469-101">Get-AzApiManagementTenantAccessSecret</span></span>

## <span data-ttu-id="51469-102">Sammanfattning</span><span class="sxs-lookup"><span data-stu-id="51469-102">SYNOPSIS</span></span>
<span data-ttu-id="51469-103">Hämtar konfigurations nycklarna för åtkomst till en klient organisation.</span><span class="sxs-lookup"><span data-stu-id="51469-103">Gets the access configuration keys for a tenant.</span></span>

## <span data-ttu-id="51469-104">FRÅGESYNTAXEN</span><span class="sxs-lookup"><span data-stu-id="51469-104">SYNTAX</span></span>

```
Get-AzApiManagementTenantAccessSecret -Context <PsApiManagementContext>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="51469-105">PROBLEMBESKRIVNING</span><span class="sxs-lookup"><span data-stu-id="51469-105">DESCRIPTION</span></span>
<span data-ttu-id="51469-106">Hämtar konfigurations nycklarna för åtkomst till en klient organisation.</span><span class="sxs-lookup"><span data-stu-id="51469-106">Gets the access configuration keys for a tenant.</span></span>

## <span data-ttu-id="51469-107">BESKRIVS</span><span class="sxs-lookup"><span data-stu-id="51469-107">EXAMPLES</span></span>

### <span data-ttu-id="51469-108">Exempel 1: hämta konfigurations nycklar för klient åtkomst</span><span class="sxs-lookup"><span data-stu-id="51469-108">Example 1: Get tenant access configuration keys</span></span>
```
PS C:\>$apimContext = New-AzApiManagementContext -ResourceGroupName "Api-Default-WestUS" -ServiceName "contoso"
PS C:\>Get-AzApiManagementTenantAccessSecret -Context $apimContext
```

<span data-ttu-id="51469-109">Det här kommandot får konfigurations nycklarna för klient åtkomst för angiven kontext.</span><span class="sxs-lookup"><span data-stu-id="51469-109">This command gets the tenant access configuration keys for the specified context.</span></span>

## <span data-ttu-id="51469-110">MALLPARAMETRAR</span><span class="sxs-lookup"><span data-stu-id="51469-110">PARAMETERS</span></span>

### <span data-ttu-id="51469-111">-Kontext</span><span class="sxs-lookup"><span data-stu-id="51469-111">-Context</span></span>
<span data-ttu-id="51469-112">Instans av PsApiManagementContext.</span><span class="sxs-lookup"><span data-stu-id="51469-112">Instance of PsApiManagementContext.</span></span>
<span data-ttu-id="51469-113">Denna parameter är obligatorisk.</span><span class="sxs-lookup"><span data-stu-id="51469-113">This parameter is required.</span></span>

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

### <span data-ttu-id="51469-114">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="51469-114">-DefaultProfile</span></span>
<span data-ttu-id="51469-115">Autentiseringsuppgifter, konto, klient organisation och abonnemang som används för kommunikation med Azure.</span><span class="sxs-lookup"><span data-stu-id="51469-115">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="51469-116">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="51469-116">CommonParameters</span></span>
<span data-ttu-id="51469-117">Den här cmdleten har stöd för de gemensamma parametrarna:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-disvariable,-utbuffer,-PipelineVariable,-verbose,-WarningAction och-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="51469-117">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="51469-118">Mer information finns i [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="51469-118">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="51469-119">KOSTNADS</span><span class="sxs-lookup"><span data-stu-id="51469-119">INPUTS</span></span>

### <span data-ttu-id="51469-120">Microsoft. Azure. commands. ApiManagement. ServiceManagement. Models. PsApiManagementContext</span><span class="sxs-lookup"><span data-stu-id="51469-120">Microsoft.Azure.Commands.ApiManagement.ServiceManagement.Models.PsApiManagementContext</span></span>

## <span data-ttu-id="51469-121">VÄRDEN</span><span class="sxs-lookup"><span data-stu-id="51469-121">OUTPUTS</span></span>

### <span data-ttu-id="51469-122">Microsoft. Azure. commands. ApiManagement. ServiceManagement. Models. PsApiManagementAccessInformation</span><span class="sxs-lookup"><span data-stu-id="51469-122">Microsoft.Azure.Commands.ApiManagement.ServiceManagement.Models.PsApiManagementAccessInformation</span></span>

## <span data-ttu-id="51469-123">ANMÄRKNINGAR</span><span class="sxs-lookup"><span data-stu-id="51469-123">NOTES</span></span>

## <span data-ttu-id="51469-124">RELATERADE LÄNKAR</span><span class="sxs-lookup"><span data-stu-id="51469-124">RELATED LINKS</span></span>
