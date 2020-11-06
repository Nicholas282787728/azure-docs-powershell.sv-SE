---
external help file: Microsoft.Azure.Commands.ApiManagement.ServiceManagement.dll-Help.xml
Module Name: AzureRM.ApiManagement
ms.assetid: 15634C76-6B34-4E2B-9354-86155827F200
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.apimanagement/new-azurermapimanagementcontext
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/ApiManagement/Commands.ApiManagement/help/New-AzureRmApiManagementContext.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/ApiManagement/Commands.ApiManagement/help/New-AzureRmApiManagementContext.md
ms.openlocfilehash: 56dc320ea6aafd37e93912071a3256040342e2db
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: sv-SE
ms.lasthandoff: 08/20/2020
ms.locfileid: "93581835"
---
# <span data-ttu-id="8c2fe-101">New-AzureRmApiManagementContext</span><span class="sxs-lookup"><span data-stu-id="8c2fe-101">New-AzureRmApiManagementContext</span></span>

## <span data-ttu-id="8c2fe-102">Sammanfattning</span><span class="sxs-lookup"><span data-stu-id="8c2fe-102">SYNOPSIS</span></span>
<span data-ttu-id="8c2fe-103">Skapar en instans av PsAzureApiManagementContext.</span><span class="sxs-lookup"><span data-stu-id="8c2fe-103">Creates an instance of PsAzureApiManagementContext.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="8c2fe-104">FRÅGESYNTAXEN</span><span class="sxs-lookup"><span data-stu-id="8c2fe-104">SYNTAX</span></span>

```
New-AzureRmApiManagementContext -ResourceGroupName <String> -ServiceName <String>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="8c2fe-105">PROBLEMBESKRIVNING</span><span class="sxs-lookup"><span data-stu-id="8c2fe-105">DESCRIPTION</span></span>
<span data-ttu-id="8c2fe-106">Cmdleten **New-AzureRmApiManagementContext** skapar en instans av **PsAzureApiManagementContext**.</span><span class="sxs-lookup"><span data-stu-id="8c2fe-106">The **New-AzureRmApiManagementContext** cmdlet creates an instance of **PsAzureApiManagementContext**.</span></span>
<span data-ttu-id="8c2fe-107">Kontexten används för alla cmdlets för API-hanterings tjänsten.</span><span class="sxs-lookup"><span data-stu-id="8c2fe-107">The context is used for all of the API Management service cmdlets.</span></span>

## <span data-ttu-id="8c2fe-108">BESKRIVS</span><span class="sxs-lookup"><span data-stu-id="8c2fe-108">EXAMPLES</span></span>

### <span data-ttu-id="8c2fe-109">Exempel 1: skapa en PsApiManagementContext-instans</span><span class="sxs-lookup"><span data-stu-id="8c2fe-109">Example 1: Create a PsApiManagementContext instance</span></span>
```
PS C:\>$ApiMgmtContext = New-AzureRmApiManagementContext -ResourceGroupName "ContosoResources" -ServiceName "Contoso"
```

<span data-ttu-id="8c2fe-110">Det här kommandot skapar en instans av **PsApiManagementContext**.</span><span class="sxs-lookup"><span data-stu-id="8c2fe-110">This command creates an instance of **PsApiManagementContext**.</span></span>

## <span data-ttu-id="8c2fe-111">MALLPARAMETRAR</span><span class="sxs-lookup"><span data-stu-id="8c2fe-111">PARAMETERS</span></span>

### <span data-ttu-id="8c2fe-112">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="8c2fe-112">-DefaultProfile</span></span>
<span data-ttu-id="8c2fe-113">Autentiseringsuppgifter, konto, klient organisation och abonnemang som används för kommunikation med Azure.</span><span class="sxs-lookup"><span data-stu-id="8c2fe-113">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="8c2fe-114">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="8c2fe-114">-ResourceGroupName</span></span>
<span data-ttu-id="8c2fe-115">Anger namnet på den resurs grupp som en API-hanterings tjänst distribueras under.</span><span class="sxs-lookup"><span data-stu-id="8c2fe-115">Specifies the name of the resource group under which an API Management service is deployed.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="8c2fe-116">-ServiceName</span><span class="sxs-lookup"><span data-stu-id="8c2fe-116">-ServiceName</span></span>
<span data-ttu-id="8c2fe-117">Anger namnet på den distribuerade API-hanterings tjänsten.</span><span class="sxs-lookup"><span data-stu-id="8c2fe-117">Specifies the name of the deployed API Management service.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="8c2fe-118">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="8c2fe-118">CommonParameters</span></span>
<span data-ttu-id="8c2fe-119">Den här cmdleten har stöd för de gemensamma parametrarna:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-disvariable,-utbuffer,-PipelineVariable,-verbose,-WarningAction och-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="8c2fe-119">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="8c2fe-120">Mer information finns i about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="8c2fe-120">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="8c2fe-121">KOSTNADS</span><span class="sxs-lookup"><span data-stu-id="8c2fe-121">INPUTS</span></span>

### <span data-ttu-id="8c2fe-122">System. String</span><span class="sxs-lookup"><span data-stu-id="8c2fe-122">System.String</span></span>

## <span data-ttu-id="8c2fe-123">VÄRDEN</span><span class="sxs-lookup"><span data-stu-id="8c2fe-123">OUTPUTS</span></span>

### <span data-ttu-id="8c2fe-124">Microsoft. Azure. commands. ApiManagement. ServiceManagement. Models. PsApiManagementContext</span><span class="sxs-lookup"><span data-stu-id="8c2fe-124">Microsoft.Azure.Commands.ApiManagement.ServiceManagement.Models.PsApiManagementContext</span></span>

## <span data-ttu-id="8c2fe-125">ANMÄRKNINGAR</span><span class="sxs-lookup"><span data-stu-id="8c2fe-125">NOTES</span></span>

## <span data-ttu-id="8c2fe-126">RELATERADE LÄNKAR</span><span class="sxs-lookup"><span data-stu-id="8c2fe-126">RELATED LINKS</span></span>
