---
external help file: Microsoft.Azure.PowerShell.Cmdlets.ApiManagement.ServiceManagement.dll-Help.xml
Module Name: Az.ApiManagement
ms.assetid: 227EF8A2-E04A-4F6B-B66E-E77F1276A7E4
online version: https://docs.microsoft.com/en-us/powershell/module/az.apimanagement/get-azapimanagementsubscriptionkey
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/ApiManagement/ApiManagement/help/Get-AzApiManagementSubscriptionKey.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/ApiManagement/ApiManagement/help/Get-AzApiManagementSubscriptionKey.md
ms.openlocfilehash: 74362c511abde8baed24f1b484a916a9e9851426
ms.sourcegitcommit: 1de2b6c3c99197958fa2101bc37680e7507f91ac
ms.translationtype: MT
ms.contentlocale: sv-SE
ms.lasthandoff: 10/13/2020
ms.locfileid: "94101790"
---
# <span data-ttu-id="72ad2-101">Get-AzApiManagementSubscriptionKey</span><span class="sxs-lookup"><span data-stu-id="72ad2-101">Get-AzApiManagementSubscriptionKey</span></span>

## <span data-ttu-id="72ad2-102">Sammanfattning</span><span class="sxs-lookup"><span data-stu-id="72ad2-102">SYNOPSIS</span></span>
<span data-ttu-id="72ad2-103">Hämtar abonnemangs nycklar.</span><span class="sxs-lookup"><span data-stu-id="72ad2-103">Gets subscription keys.</span></span>

## <span data-ttu-id="72ad2-104">FRÅGESYNTAXEN</span><span class="sxs-lookup"><span data-stu-id="72ad2-104">SYNTAX</span></span>

```
Get-AzApiManagementSubscriptionKey -Context <PsApiManagementContext> -SubscriptionId <String>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="72ad2-105">PROBLEMBESKRIVNING</span><span class="sxs-lookup"><span data-stu-id="72ad2-105">DESCRIPTION</span></span>
<span data-ttu-id="72ad2-106">Cmdleten **Get-AzApiManagementSubscriptionKey** hämtar en nyckel för ett angivet abonnemang.</span><span class="sxs-lookup"><span data-stu-id="72ad2-106">The **Get-AzApiManagementSubscriptionKey** cmdlet gets a keys of a specified subscription.</span></span>

## <span data-ttu-id="72ad2-107">BESKRIVS</span><span class="sxs-lookup"><span data-stu-id="72ad2-107">EXAMPLES</span></span>

### <span data-ttu-id="72ad2-108">Exempel 1: Hämta ett abonnemang med ett angivet ID</span><span class="sxs-lookup"><span data-stu-id="72ad2-108">Example 1: Get a subscription keys with a specified ID</span></span>
```
PS C:\>$apimContext = New-AzApiManagementContext -ResourceGroupName "Api-Default-East-US" -ServiceName "contoso"
PS C:\>Get-AzApiManagementSubscriptionKey -Context $apimContext -SubscriptionId "0123456789"

PrimaryKey        : 5e48532634114fe999a6979ce0d63a64
SecondaryKey      : 0a8efaf85a664aa0a412241015c7c8f6
```

<span data-ttu-id="72ad2-109">Det här kommandot får ett abonnemang utifrån ID.</span><span class="sxs-lookup"><span data-stu-id="72ad2-109">This command gets a subscription by ID.</span></span>

## <span data-ttu-id="72ad2-110">MALLPARAMETRAR</span><span class="sxs-lookup"><span data-stu-id="72ad2-110">PARAMETERS</span></span>

### <span data-ttu-id="72ad2-111">-Kontext</span><span class="sxs-lookup"><span data-stu-id="72ad2-111">-Context</span></span>
<span data-ttu-id="72ad2-112">Anger ett **PsApiManagementContext** -objekt.</span><span class="sxs-lookup"><span data-stu-id="72ad2-112">Specifies a **PsApiManagementContext** object.</span></span>

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

### <span data-ttu-id="72ad2-113">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="72ad2-113">-DefaultProfile</span></span>
<span data-ttu-id="72ad2-114">Autentiseringsuppgifter, konto, klient organisation och abonnemang som används för kommunikation med Azure.</span><span class="sxs-lookup"><span data-stu-id="72ad2-114">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="72ad2-115">-SubscriptionId</span><span class="sxs-lookup"><span data-stu-id="72ad2-115">-SubscriptionId</span></span>
<span data-ttu-id="72ad2-116">Anger en prenumerations-ID.</span><span class="sxs-lookup"><span data-stu-id="72ad2-116">Specifies a subscription identifier.</span></span>
<span data-ttu-id="72ad2-117">Om du anger den här cmdleten hittar den en prenumeration utifrån identifieraren.</span><span class="sxs-lookup"><span data-stu-id="72ad2-117">If specified, this cmdlet finds subscription by the identifier.</span></span>

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

### <span data-ttu-id="72ad2-118">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="72ad2-118">CommonParameters</span></span>
<span data-ttu-id="72ad2-119">Den här cmdleten har stöd för de gemensamma parametrarna:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-disvariable,-utbuffer,-PipelineVariable,-verbose,-WarningAction och-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="72ad2-119">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="72ad2-120">Mer information finns i [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="72ad2-120">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="72ad2-121">KOSTNADS</span><span class="sxs-lookup"><span data-stu-id="72ad2-121">INPUTS</span></span>

### <span data-ttu-id="72ad2-122">Microsoft. Azure. commands. ApiManagement. ServiceManagement. Models. PsApiManagementContext</span><span class="sxs-lookup"><span data-stu-id="72ad2-122">Microsoft.Azure.Commands.ApiManagement.ServiceManagement.Models.PsApiManagementContext</span></span>

### <span data-ttu-id="72ad2-123">System. String</span><span class="sxs-lookup"><span data-stu-id="72ad2-123">System.String</span></span>

## <span data-ttu-id="72ad2-124">VÄRDEN</span><span class="sxs-lookup"><span data-stu-id="72ad2-124">OUTPUTS</span></span>

### <span data-ttu-id="72ad2-125">Microsoft. Azure. commands. ApiManagement. ServiceManagement. Models. PsApiManagementSubscriptionKey</span><span class="sxs-lookup"><span data-stu-id="72ad2-125">Microsoft.Azure.Commands.ApiManagement.ServiceManagement.Models.PsApiManagementSubscriptionKey</span></span>

## <span data-ttu-id="72ad2-126">ANMÄRKNINGAR</span><span class="sxs-lookup"><span data-stu-id="72ad2-126">NOTES</span></span>

## <span data-ttu-id="72ad2-127">RELATERADE LÄNKAR</span><span class="sxs-lookup"><span data-stu-id="72ad2-127">RELATED LINKS</span></span>

[<span data-ttu-id="72ad2-128">New-AzApiManagementSubscription</span><span class="sxs-lookup"><span data-stu-id="72ad2-128">New-AzApiManagementSubscription</span></span>](./Get-AzApiManagementSubscription.md)

[<span data-ttu-id="72ad2-129">New-AzApiManagementSubscription</span><span class="sxs-lookup"><span data-stu-id="72ad2-129">New-AzApiManagementSubscription</span></span>](./New-AzApiManagementSubscription.md)

[<span data-ttu-id="72ad2-130">Remove-AzApiManagementSubscription</span><span class="sxs-lookup"><span data-stu-id="72ad2-130">Remove-AzApiManagementSubscription</span></span>](./Remove-AzApiManagementSubscription.md)

[<span data-ttu-id="72ad2-131">Set-AzApiManagementSubscription</span><span class="sxs-lookup"><span data-stu-id="72ad2-131">Set-AzApiManagementSubscription</span></span>](./Set-AzApiManagementSubscription.md)


