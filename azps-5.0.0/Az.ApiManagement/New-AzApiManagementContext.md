---
external help file: Microsoft.Azure.PowerShell.Cmdlets.ApiManagement.ServiceManagement.dll-Help.xml
Module Name: Az.ApiManagement
ms.assetid: 15634C76-6B34-4E2B-9354-86155827F200
online version: https://docs.microsoft.com/en-us/powershell/module/az.apimanagement/new-azapimanagementcontext
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/ApiManagement/ApiManagement/help/New-AzApiManagementContext.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/ApiManagement/ApiManagement/help/New-AzApiManagementContext.md
ms.openlocfilehash: 060f58bc0206ea02f17239b6787f3a854aa3cb94
ms.sourcegitcommit: b4a38bcb0501a9016a4998efd377aa75d3ef9ce8
ms.translationtype: MT
ms.contentlocale: sv-SE
ms.lasthandoff: 10/27/2020
ms.locfileid: "94270742"
---
# <span data-ttu-id="98abb-101">New-AzApiManagementContext</span><span class="sxs-lookup"><span data-stu-id="98abb-101">New-AzApiManagementContext</span></span>

## <span data-ttu-id="98abb-102">Sammanfattning</span><span class="sxs-lookup"><span data-stu-id="98abb-102">SYNOPSIS</span></span>
<span data-ttu-id="98abb-103">Skapar en instans av PsAzureApiManagementContext.</span><span class="sxs-lookup"><span data-stu-id="98abb-103">Creates an instance of PsAzureApiManagementContext.</span></span>

## <span data-ttu-id="98abb-104">FRÅGESYNTAXEN</span><span class="sxs-lookup"><span data-stu-id="98abb-104">SYNTAX</span></span>

### <span data-ttu-id="98abb-105">ContextParameterSet (standard)</span><span class="sxs-lookup"><span data-stu-id="98abb-105">ContextParameterSet (Default)</span></span>
```
New-AzApiManagementContext -ResourceGroupName <String> -ServiceName <String>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="98abb-106">ResourceIdParameterSet</span><span class="sxs-lookup"><span data-stu-id="98abb-106">ResourceIdParameterSet</span></span>
```
New-AzApiManagementContext -ResourceId <String> [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="98abb-107">PROBLEMBESKRIVNING</span><span class="sxs-lookup"><span data-stu-id="98abb-107">DESCRIPTION</span></span>
<span data-ttu-id="98abb-108">Cmdleten **New-AzApiManagementContext** skapar en instans av **PsAzureApiManagementContext**.</span><span class="sxs-lookup"><span data-stu-id="98abb-108">The **New-AzApiManagementContext** cmdlet creates an instance of **PsAzureApiManagementContext**.</span></span>
<span data-ttu-id="98abb-109">Kontexten används för alla cmdlets för API-hanterings tjänsten.</span><span class="sxs-lookup"><span data-stu-id="98abb-109">The context is used for all of the API Management service cmdlets.</span></span>

## <span data-ttu-id="98abb-110">BESKRIVS</span><span class="sxs-lookup"><span data-stu-id="98abb-110">EXAMPLES</span></span>

### <span data-ttu-id="98abb-111">Exempel 1: skapa en PsApiManagementContext-instans</span><span class="sxs-lookup"><span data-stu-id="98abb-111">Example 1: Create a PsApiManagementContext instance</span></span>
```
PS C:\>$ApiMgmtContext = New-AzApiManagementContext -ResourceGroupName "ContosoResources" -ServiceName "Contoso"
```

<span data-ttu-id="98abb-112">Det här kommandot skapar en instans av **PsApiManagementContext**.</span><span class="sxs-lookup"><span data-stu-id="98abb-112">This command creates an instance of **PsApiManagementContext**.</span></span>

## <span data-ttu-id="98abb-113">MALLPARAMETRAR</span><span class="sxs-lookup"><span data-stu-id="98abb-113">PARAMETERS</span></span>

### <span data-ttu-id="98abb-114">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="98abb-114">-DefaultProfile</span></span>
<span data-ttu-id="98abb-115">Autentiseringsuppgifter, konto, klient organisation och abonnemang som används för kommunikation med Azure.</span><span class="sxs-lookup"><span data-stu-id="98abb-115">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="98abb-116">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="98abb-116">-ResourceGroupName</span></span>
<span data-ttu-id="98abb-117">Anger namnet på den resurs grupp som en API-hanterings tjänst distribueras under.</span><span class="sxs-lookup"><span data-stu-id="98abb-117">Specifies the name of the resource group under which an API Management service is deployed.</span></span>

```yaml
Type: System.String
Parameter Sets: ContextParameterSet
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="98abb-118">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="98abb-118">-ResourceId</span></span>
<span data-ttu-id="98abb-119">Arm-resurs-ID för en ApiManagement-tjänst.</span><span class="sxs-lookup"><span data-stu-id="98abb-119">Arm Resource Identifier of a ApiManagement service.</span></span> <span data-ttu-id="98abb-120">Denna parameter är obligatorisk.</span><span class="sxs-lookup"><span data-stu-id="98abb-120">This parameter is required.</span></span>

```yaml
Type: System.String
Parameter Sets: ResourceIdParameterSet
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="98abb-121">-ServiceName</span><span class="sxs-lookup"><span data-stu-id="98abb-121">-ServiceName</span></span>
<span data-ttu-id="98abb-122">Anger namnet på den distribuerade API-hanterings tjänsten.</span><span class="sxs-lookup"><span data-stu-id="98abb-122">Specifies the name of the deployed API Management service.</span></span>

```yaml
Type: System.String
Parameter Sets: ContextParameterSet
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="98abb-123">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="98abb-123">CommonParameters</span></span>
<span data-ttu-id="98abb-124">Den här cmdleten har stöd för de gemensamma parametrarna:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-disvariable,-utbuffer,-PipelineVariable,-verbose,-WarningAction och-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="98abb-124">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="98abb-125">Mer information finns i [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="98abb-125">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="98abb-126">KOSTNADS</span><span class="sxs-lookup"><span data-stu-id="98abb-126">INPUTS</span></span>

### <span data-ttu-id="98abb-127">System. String</span><span class="sxs-lookup"><span data-stu-id="98abb-127">System.String</span></span>

## <span data-ttu-id="98abb-128">VÄRDEN</span><span class="sxs-lookup"><span data-stu-id="98abb-128">OUTPUTS</span></span>

### <span data-ttu-id="98abb-129">Microsoft. Azure. commands. ApiManagement. ServiceManagement. Models. PsApiManagementContext</span><span class="sxs-lookup"><span data-stu-id="98abb-129">Microsoft.Azure.Commands.ApiManagement.ServiceManagement.Models.PsApiManagementContext</span></span>

## <span data-ttu-id="98abb-130">ANMÄRKNINGAR</span><span class="sxs-lookup"><span data-stu-id="98abb-130">NOTES</span></span>

## <span data-ttu-id="98abb-131">RELATERADE LÄNKAR</span><span class="sxs-lookup"><span data-stu-id="98abb-131">RELATED LINKS</span></span>