---
external help file: Microsoft.Azure.PowerShell.Cmdlets.ApiManagement.ServiceManagement.dll-Help.xml
Module Name: Az.ApiManagement
online version: https://docs.microsoft.com/en-us/powershell/module/az.apimanagement/get-azapimanagementgatewaykey
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/ApiManagement/ApiManagement/help/Get-AzApiManagementGatewayKey.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/ApiManagement/ApiManagement/help/Get-AzApiManagementGatewayKey.md
ms.openlocfilehash: d58d33789f491098a62d7628ce6495ef2ba8870b
ms.sourcegitcommit: b4a38bcb0501a9016a4998efd377aa75d3ef9ce8
ms.translationtype: MT
ms.contentlocale: sv-SE
ms.lasthandoff: 10/27/2020
ms.locfileid: "94321939"
---
# <span data-ttu-id="737c7-101">Get-AzApiManagementGatewayKey</span><span class="sxs-lookup"><span data-stu-id="737c7-101">Get-AzApiManagementGatewayKey</span></span>

## <span data-ttu-id="737c7-102">Sammanfattning</span><span class="sxs-lookup"><span data-stu-id="737c7-102">SYNOPSIS</span></span>
<span data-ttu-id="737c7-103">Hämtar nycklar för den befintliga gatewayen</span><span class="sxs-lookup"><span data-stu-id="737c7-103">Gets keys of the existing Gateway</span></span>

## <span data-ttu-id="737c7-104">FRÅGESYNTAXEN</span><span class="sxs-lookup"><span data-stu-id="737c7-104">SYNTAX</span></span>

```
Get-AzApiManagementGatewayKey -Context <PsApiManagementContext> -GatewayId <String>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="737c7-105">PROBLEMBESKRIVNING</span><span class="sxs-lookup"><span data-stu-id="737c7-105">DESCRIPTION</span></span>
<span data-ttu-id="737c7-106">Cmdleten **Get-AzApiManagementGatewayKey** hämtar nycklarna till den befintliga gatewayen</span><span class="sxs-lookup"><span data-stu-id="737c7-106">The **Get-AzApiManagementGatewayKey** cmdlet gets keys of the existing Gateway</span></span>

## <span data-ttu-id="737c7-107">BESKRIVS</span><span class="sxs-lookup"><span data-stu-id="737c7-107">EXAMPLES</span></span>

### <span data-ttu-id="737c7-108">Exempel 2: skaffa en gateway utifrån ID</span><span class="sxs-lookup"><span data-stu-id="737c7-108">Example 2: Get a gateway by ID</span></span>
```
PS C:\>$apimContext = New-AzApiManagementContext -ResourceGroupName "Api-Default-WestUS" -ServiceName "contoso"
PS C:\>Get-AzApiManagementGatewayKey -Context $apimContext -GatewayId "0123456789"
```

<span data-ttu-id="737c7-109">Det här kommandot får nycklarna till en "0123456789"-Gateway.</span><span class="sxs-lookup"><span data-stu-id="737c7-109">This command gets the keys for a "0123456789" gateway.</span></span>

## <span data-ttu-id="737c7-110">MALLPARAMETRAR</span><span class="sxs-lookup"><span data-stu-id="737c7-110">PARAMETERS</span></span>

### <span data-ttu-id="737c7-111">-Kontext</span><span class="sxs-lookup"><span data-stu-id="737c7-111">-Context</span></span>
<span data-ttu-id="737c7-112">Instans av PsApiManagementContext.</span><span class="sxs-lookup"><span data-stu-id="737c7-112">Instance of PsApiManagementContext.</span></span>
<span data-ttu-id="737c7-113">Denna parameter är obligatorisk.</span><span class="sxs-lookup"><span data-stu-id="737c7-113">This parameter is required.</span></span>

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

### <span data-ttu-id="737c7-114">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="737c7-114">-DefaultProfile</span></span>
<span data-ttu-id="737c7-115">Autentiseringsuppgifter, konto, klient organisation och abonnemang som används för kommunikation med Azure.</span><span class="sxs-lookup"><span data-stu-id="737c7-115">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="737c7-116">-GatewayId</span><span class="sxs-lookup"><span data-stu-id="737c7-116">-GatewayId</span></span>
<span data-ttu-id="737c7-117">Gateway-ID.</span><span class="sxs-lookup"><span data-stu-id="737c7-117">Gateway identifier.</span></span>
<span data-ttu-id="737c7-118">Denna parameter är obligatorisk.</span><span class="sxs-lookup"><span data-stu-id="737c7-118">This parameter is required.</span></span>

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

### <span data-ttu-id="737c7-119">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="737c7-119">CommonParameters</span></span>
<span data-ttu-id="737c7-120">Den här cmdleten har stöd för de gemensamma parametrarna:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-disvariable,-utbuffer,-PipelineVariable,-verbose,-WarningAction och-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="737c7-120">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="737c7-121">Mer information finns i [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="737c7-121">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="737c7-122">KOSTNADS</span><span class="sxs-lookup"><span data-stu-id="737c7-122">INPUTS</span></span>

### <span data-ttu-id="737c7-123">Microsoft. Azure. commands. ApiManagement. ServiceManagement. Models. PsApiManagementContext</span><span class="sxs-lookup"><span data-stu-id="737c7-123">Microsoft.Azure.Commands.ApiManagement.ServiceManagement.Models.PsApiManagementContext</span></span>

### <span data-ttu-id="737c7-124">System. String</span><span class="sxs-lookup"><span data-stu-id="737c7-124">System.String</span></span>

## <span data-ttu-id="737c7-125">VÄRDEN</span><span class="sxs-lookup"><span data-stu-id="737c7-125">OUTPUTS</span></span>

### <span data-ttu-id="737c7-126">Microsoft. Azure. commands. ApiManagement. ServiceManagement. Models. PsApiManagementGatewayKey</span><span class="sxs-lookup"><span data-stu-id="737c7-126">Microsoft.Azure.Commands.ApiManagement.ServiceManagement.Models.PsApiManagementGatewayKey</span></span>

## <span data-ttu-id="737c7-127">ANMÄRKNINGAR</span><span class="sxs-lookup"><span data-stu-id="737c7-127">NOTES</span></span>

## <span data-ttu-id="737c7-128">RELATERADE LÄNKAR</span><span class="sxs-lookup"><span data-stu-id="737c7-128">RELATED LINKS</span></span>
