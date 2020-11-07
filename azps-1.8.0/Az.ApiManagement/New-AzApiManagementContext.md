---
external help file: Microsoft.Azure.PowerShell.Cmdlets.ApiManagement.ServiceManagement.dll-Help.xml
Module Name: Az.ApiManagement
ms.assetid: 15634C76-6B34-4E2B-9354-86155827F200
online version: https://docs.microsoft.com/en-us/powershell/module/az.apimanagement/new-azapimanagementcontext
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/ApiManagement/ApiManagement/help/New-AzApiManagementContext.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/ApiManagement/ApiManagement/help/New-AzApiManagementContext.md
ms.openlocfilehash: cec27d1f7fb83cb114cd4b9a5c508c807e8ebd5c
ms.sourcegitcommit: 4d2c178cd6df9151877b08d54c1f4a228dbec9d1
ms.translationtype: MT
ms.contentlocale: sv-SE
ms.lasthandoff: 01/29/2020
ms.locfileid: "93754905"
---
# <span data-ttu-id="bfae0-101">New-AzApiManagementContext</span><span class="sxs-lookup"><span data-stu-id="bfae0-101">New-AzApiManagementContext</span></span>

## <span data-ttu-id="bfae0-102">Sammanfattning</span><span class="sxs-lookup"><span data-stu-id="bfae0-102">SYNOPSIS</span></span>
<span data-ttu-id="bfae0-103">Skapar en instans av PsAzureApiManagementContext.</span><span class="sxs-lookup"><span data-stu-id="bfae0-103">Creates an instance of PsAzureApiManagementContext.</span></span>

## <span data-ttu-id="bfae0-104">FRÅGESYNTAXEN</span><span class="sxs-lookup"><span data-stu-id="bfae0-104">SYNTAX</span></span>

```
New-AzApiManagementContext -ResourceGroupName <String> -ServiceName <String>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="bfae0-105">PROBLEMBESKRIVNING</span><span class="sxs-lookup"><span data-stu-id="bfae0-105">DESCRIPTION</span></span>
<span data-ttu-id="bfae0-106">Cmdleten **New-AzApiManagementContext** skapar en instans av **PsAzureApiManagementContext**.</span><span class="sxs-lookup"><span data-stu-id="bfae0-106">The **New-AzApiManagementContext** cmdlet creates an instance of **PsAzureApiManagementContext**.</span></span>
<span data-ttu-id="bfae0-107">Kontexten används för alla cmdlets för API-hanterings tjänsten.</span><span class="sxs-lookup"><span data-stu-id="bfae0-107">The context is used for all of the API Management service cmdlets.</span></span>

## <span data-ttu-id="bfae0-108">BESKRIVS</span><span class="sxs-lookup"><span data-stu-id="bfae0-108">EXAMPLES</span></span>

### <span data-ttu-id="bfae0-109">Exempel 1: skapa en PsApiManagementContext-instans</span><span class="sxs-lookup"><span data-stu-id="bfae0-109">Example 1: Create a PsApiManagementContext instance</span></span>
```
PS C:\>$ApiMgmtContext = New-AzApiManagementContext -ResourceGroupName "ContosoResources" -ServiceName "Contoso"
```

<span data-ttu-id="bfae0-110">Det här kommandot skapar en instans av **PsApiManagementContext**.</span><span class="sxs-lookup"><span data-stu-id="bfae0-110">This command creates an instance of **PsApiManagementContext**.</span></span>

## <span data-ttu-id="bfae0-111">MALLPARAMETRAR</span><span class="sxs-lookup"><span data-stu-id="bfae0-111">PARAMETERS</span></span>

### <span data-ttu-id="bfae0-112">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="bfae0-112">-DefaultProfile</span></span>
<span data-ttu-id="bfae0-113">Autentiseringsuppgifter, konto, klient organisation och abonnemang som används för kommunikation med Azure.</span><span class="sxs-lookup"><span data-stu-id="bfae0-113">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="bfae0-114">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="bfae0-114">-ResourceGroupName</span></span>
<span data-ttu-id="bfae0-115">Anger namnet på den resurs grupp som en API-hanterings tjänst distribueras under.</span><span class="sxs-lookup"><span data-stu-id="bfae0-115">Specifies the name of the resource group under which an API Management service is deployed.</span></span>

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

### <span data-ttu-id="bfae0-116">-ServiceName</span><span class="sxs-lookup"><span data-stu-id="bfae0-116">-ServiceName</span></span>
<span data-ttu-id="bfae0-117">Anger namnet på den distribuerade API-hanterings tjänsten.</span><span class="sxs-lookup"><span data-stu-id="bfae0-117">Specifies the name of the deployed API Management service.</span></span>

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

### <span data-ttu-id="bfae0-118">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="bfae0-118">CommonParameters</span></span>
<span data-ttu-id="bfae0-119">Den här cmdleten har stöd för de gemensamma parametrarna:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-disvariable,-utbuffer,-PipelineVariable,-verbose,-WarningAction och-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="bfae0-119">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="bfae0-120">Mer information finns i about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="bfae0-120">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="bfae0-121">KOSTNADS</span><span class="sxs-lookup"><span data-stu-id="bfae0-121">INPUTS</span></span>

### <span data-ttu-id="bfae0-122">System. String</span><span class="sxs-lookup"><span data-stu-id="bfae0-122">System.String</span></span>

## <span data-ttu-id="bfae0-123">VÄRDEN</span><span class="sxs-lookup"><span data-stu-id="bfae0-123">OUTPUTS</span></span>

### <span data-ttu-id="bfae0-124">Microsoft. Azure. commands. ApiManagement. ServiceManagement. Models. PsApiManagementContext</span><span class="sxs-lookup"><span data-stu-id="bfae0-124">Microsoft.Azure.Commands.ApiManagement.ServiceManagement.Models.PsApiManagementContext</span></span>

## <span data-ttu-id="bfae0-125">ANMÄRKNINGAR</span><span class="sxs-lookup"><span data-stu-id="bfae0-125">NOTES</span></span>

## <span data-ttu-id="bfae0-126">RELATERADE LÄNKAR</span><span class="sxs-lookup"><span data-stu-id="bfae0-126">RELATED LINKS</span></span>
