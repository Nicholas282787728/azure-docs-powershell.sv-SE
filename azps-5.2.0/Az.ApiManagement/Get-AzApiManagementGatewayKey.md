---
external help file: Microsoft.Azure.PowerShell.Cmdlets.ApiManagement.ServiceManagement.dll-Help.xml
Module Name: Az.ApiManagement
online version: https://docs.microsoft.com/en-us/powershell/module/az.apimanagement/get-azapimanagementgatewaykey
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/ApiManagement/ApiManagement/help/Get-AzApiManagementGatewayKey.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/ApiManagement/ApiManagement/help/Get-AzApiManagementGatewayKey.md
ms.openlocfilehash: d58d33789f491098a62d7628ce6495ef2ba8870b
ms.sourcegitcommit: 04221336bc9eed46c05ed1e828a6811534d4b4ab
ms.translationtype: MT
ms.contentlocale: sv-SE
ms.lasthandoff: 12/08/2020
ms.locfileid: "98413883"
---
# <span data-ttu-id="7a254-101">Get-AzApiManagementGatewayKey</span><span class="sxs-lookup"><span data-stu-id="7a254-101">Get-AzApiManagementGatewayKey</span></span>

## <span data-ttu-id="7a254-102">Sammanfattning</span><span class="sxs-lookup"><span data-stu-id="7a254-102">SYNOPSIS</span></span>
<span data-ttu-id="7a254-103">Hämtar nycklar för den befintliga gatewayen</span><span class="sxs-lookup"><span data-stu-id="7a254-103">Gets keys of the existing Gateway</span></span>

## <span data-ttu-id="7a254-104">FRÅGESYNTAXEN</span><span class="sxs-lookup"><span data-stu-id="7a254-104">SYNTAX</span></span>

```
Get-AzApiManagementGatewayKey -Context <PsApiManagementContext> -GatewayId <String>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="7a254-105">PROBLEMBESKRIVNING</span><span class="sxs-lookup"><span data-stu-id="7a254-105">DESCRIPTION</span></span>
<span data-ttu-id="7a254-106">Cmdleten **Get-AzApiManagementGatewayKey** hämtar nycklarna till den befintliga gatewayen</span><span class="sxs-lookup"><span data-stu-id="7a254-106">The **Get-AzApiManagementGatewayKey** cmdlet gets keys of the existing Gateway</span></span>

## <span data-ttu-id="7a254-107">BESKRIVS</span><span class="sxs-lookup"><span data-stu-id="7a254-107">EXAMPLES</span></span>

### <span data-ttu-id="7a254-108">Exempel 2: skaffa en gateway utifrån ID</span><span class="sxs-lookup"><span data-stu-id="7a254-108">Example 2: Get a gateway by ID</span></span>
```
PS C:\>$apimContext = New-AzApiManagementContext -ResourceGroupName "Api-Default-WestUS" -ServiceName "contoso"
PS C:\>Get-AzApiManagementGatewayKey -Context $apimContext -GatewayId "0123456789"
```

<span data-ttu-id="7a254-109">Det här kommandot får nycklarna till en "0123456789"-Gateway.</span><span class="sxs-lookup"><span data-stu-id="7a254-109">This command gets the keys for a "0123456789" gateway.</span></span>

## <span data-ttu-id="7a254-110">MALLPARAMETRAR</span><span class="sxs-lookup"><span data-stu-id="7a254-110">PARAMETERS</span></span>

### <span data-ttu-id="7a254-111">-Kontext</span><span class="sxs-lookup"><span data-stu-id="7a254-111">-Context</span></span>
<span data-ttu-id="7a254-112">Instans av PsApiManagementContext.</span><span class="sxs-lookup"><span data-stu-id="7a254-112">Instance of PsApiManagementContext.</span></span>
<span data-ttu-id="7a254-113">Denna parameter är obligatorisk.</span><span class="sxs-lookup"><span data-stu-id="7a254-113">This parameter is required.</span></span>

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

### <span data-ttu-id="7a254-114">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="7a254-114">-DefaultProfile</span></span>
<span data-ttu-id="7a254-115">Autentiseringsuppgifter, konto, klient organisation och abonnemang som används för kommunikation med Azure.</span><span class="sxs-lookup"><span data-stu-id="7a254-115">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="7a254-116">-GatewayId</span><span class="sxs-lookup"><span data-stu-id="7a254-116">-GatewayId</span></span>
<span data-ttu-id="7a254-117">Gateway-ID.</span><span class="sxs-lookup"><span data-stu-id="7a254-117">Gateway identifier.</span></span>
<span data-ttu-id="7a254-118">Denna parameter är obligatorisk.</span><span class="sxs-lookup"><span data-stu-id="7a254-118">This parameter is required.</span></span>

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

### <span data-ttu-id="7a254-119">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="7a254-119">CommonParameters</span></span>
<span data-ttu-id="7a254-120">Den här cmdleten har stöd för de gemensamma parametrarna:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-disvariable,-utbuffer,-PipelineVariable,-verbose,-WarningAction och-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="7a254-120">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="7a254-121">Mer information finns i [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="7a254-121">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="7a254-122">KOSTNADS</span><span class="sxs-lookup"><span data-stu-id="7a254-122">INPUTS</span></span>

### <span data-ttu-id="7a254-123">Microsoft. Azure. commands. ApiManagement. ServiceManagement. Models. PsApiManagementContext</span><span class="sxs-lookup"><span data-stu-id="7a254-123">Microsoft.Azure.Commands.ApiManagement.ServiceManagement.Models.PsApiManagementContext</span></span>

### <span data-ttu-id="7a254-124">System. String</span><span class="sxs-lookup"><span data-stu-id="7a254-124">System.String</span></span>

## <span data-ttu-id="7a254-125">VÄRDEN</span><span class="sxs-lookup"><span data-stu-id="7a254-125">OUTPUTS</span></span>

### <span data-ttu-id="7a254-126">Microsoft. Azure. commands. ApiManagement. ServiceManagement. Models. PsApiManagementGatewayKey</span><span class="sxs-lookup"><span data-stu-id="7a254-126">Microsoft.Azure.Commands.ApiManagement.ServiceManagement.Models.PsApiManagementGatewayKey</span></span>

## <span data-ttu-id="7a254-127">ANMÄRKNINGAR</span><span class="sxs-lookup"><span data-stu-id="7a254-127">NOTES</span></span>

## <span data-ttu-id="7a254-128">RELATERADE LÄNKAR</span><span class="sxs-lookup"><span data-stu-id="7a254-128">RELATED LINKS</span></span>
