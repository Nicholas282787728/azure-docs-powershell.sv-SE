---
external help file: Microsoft.Azure.Commands.ApiManagement.ServiceManagement.dll-Help.xml
ms.assetid: 15634C76-6B34-4E2B-9354-86155827F200
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.apimanagement/new-azurermapimanagementcontext
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/ApiManagement/Commands.ApiManagement/help/New-AzureRmApiManagementContext.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/ApiManagement/Commands.ApiManagement/help/New-AzureRmApiManagementContext.md
ms.openlocfilehash: da9924624065937a0cb2d78160b1a12cb698a42d
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: sv-SE
ms.lasthandoff: 08/20/2020
ms.locfileid: "93576646"
---
# <span data-ttu-id="29328-101">New-AzureRmApiManagementContext</span><span class="sxs-lookup"><span data-stu-id="29328-101">New-AzureRmApiManagementContext</span></span>

## <span data-ttu-id="29328-102">Sammanfattning</span><span class="sxs-lookup"><span data-stu-id="29328-102">SYNOPSIS</span></span>
<span data-ttu-id="29328-103">Skapar en instans av PsAzureApiManagementContext.</span><span class="sxs-lookup"><span data-stu-id="29328-103">Creates an instance of PsAzureApiManagementContext.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="29328-104">FRÅGESYNTAXEN</span><span class="sxs-lookup"><span data-stu-id="29328-104">SYNTAX</span></span>

```
New-AzureRmApiManagementContext -ResourceGroupName <String> -ServiceName <String>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="29328-105">PROBLEMBESKRIVNING</span><span class="sxs-lookup"><span data-stu-id="29328-105">DESCRIPTION</span></span>
<span data-ttu-id="29328-106">Cmdleten **New-AzureRmApiManagementContext** skapar en instans av **PsAzureApiManagementContext**.</span><span class="sxs-lookup"><span data-stu-id="29328-106">The **New-AzureRmApiManagementContext** cmdlet creates an instance of **PsAzureApiManagementContext**.</span></span>
<span data-ttu-id="29328-107">Kontexten används för alla cmdlets för API-hanterings tjänsten.</span><span class="sxs-lookup"><span data-stu-id="29328-107">The context is used for all of the API Management service cmdlets.</span></span>

## <span data-ttu-id="29328-108">BESKRIVS</span><span class="sxs-lookup"><span data-stu-id="29328-108">EXAMPLES</span></span>

### <span data-ttu-id="29328-109">Exempel 1: skapa en PsApiManagementContext-instans</span><span class="sxs-lookup"><span data-stu-id="29328-109">Example 1: Create a PsApiManagementContext instance</span></span>
```
PS C:\>$ApiMgmtContext = New-AzureRmApiManagementContext -ResourceGroupName "ContosoResources" -ServiceName "Contoso"
```

<span data-ttu-id="29328-110">Det här kommandot skapar en instans av **PsApiManagementContext**.</span><span class="sxs-lookup"><span data-stu-id="29328-110">This command creates an instance of **PsApiManagementContext**.</span></span>

## <span data-ttu-id="29328-111">MALLPARAMETRAR</span><span class="sxs-lookup"><span data-stu-id="29328-111">PARAMETERS</span></span>

### <span data-ttu-id="29328-112">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="29328-112">-DefaultProfile</span></span>
<span data-ttu-id="29328-113">Autentiseringsuppgifter, konto, klient organisation och abonnemang som används för kommunikation med Azure.</span><span class="sxs-lookup"><span data-stu-id="29328-113">The credentials, account, tenant, and subscription used for communication with azure.</span></span>
 
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

### <span data-ttu-id="29328-114">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="29328-114">-ResourceGroupName</span></span>
<span data-ttu-id="29328-115">Anger namnet på den resurs grupp som en API-hanterings tjänst distribueras under.</span><span class="sxs-lookup"><span data-stu-id="29328-115">Specifies the name of the resource group under which an API Management service is deployed.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="29328-116">-ServiceName</span><span class="sxs-lookup"><span data-stu-id="29328-116">-ServiceName</span></span>
<span data-ttu-id="29328-117">Anger namnet på den distribuerade API-hanterings tjänsten.</span><span class="sxs-lookup"><span data-stu-id="29328-117">Specifies the name of the deployed API Management service.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="29328-118">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="29328-118">CommonParameters</span></span>
<span data-ttu-id="29328-119">Den här cmdleten har stöd för de gemensamma parametrarna:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-disvariable,-utbuffer,-PipelineVariable,-verbose,-WarningAction och-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="29328-119">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="29328-120">Mer information finns i about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="29328-120">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="29328-121">KOSTNADS</span><span class="sxs-lookup"><span data-stu-id="29328-121">INPUTS</span></span>

### <span data-ttu-id="29328-122">Ingen</span><span class="sxs-lookup"><span data-stu-id="29328-122">None</span></span>
<span data-ttu-id="29328-123">Denna cmdlet accepterar inte indata.</span><span class="sxs-lookup"><span data-stu-id="29328-123">This cmdlet does not accept any input.</span></span>

## <span data-ttu-id="29328-124">VÄRDEN</span><span class="sxs-lookup"><span data-stu-id="29328-124">OUTPUTS</span></span>

### <span data-ttu-id="29328-125">Microsoft. Azure. commands. ApiManagement. ServiceManagement. Models. PsAzureApiManagementContext</span><span class="sxs-lookup"><span data-stu-id="29328-125">Microsoft.Azure.Commands.ApiManagement.ServiceManagement.Models.PsAzureApiManagementContext</span></span>

## <span data-ttu-id="29328-126">ANMÄRKNINGAR</span><span class="sxs-lookup"><span data-stu-id="29328-126">NOTES</span></span>

## <span data-ttu-id="29328-127">RELATERADE LÄNKAR</span><span class="sxs-lookup"><span data-stu-id="29328-127">RELATED LINKS</span></span>

