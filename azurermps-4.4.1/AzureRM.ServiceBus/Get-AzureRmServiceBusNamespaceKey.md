---
external help file: Microsoft.Azure.Commands.ServiceBus.dll-Help.xml
Module Name: AzureRM.ServiceBus
online version: ''
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/ServiceBus/Commands.ServiceBus/help/Get-AzureRmServiceBusNamespaceKey.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/ServiceBus/Commands.ServiceBus/help/Get-AzureRmServiceBusNamespaceKey.md
ms.openlocfilehash: 87dc2d1e372bdab6415a78e8c79ed0c3bd5491ed
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: sv-SE
ms.lasthandoff: 08/20/2020
ms.locfileid: "93577436"
---
# <span data-ttu-id="25f59-101">Get-AzureRmServiceBusNamespaceKey</span><span class="sxs-lookup"><span data-stu-id="25f59-101">Get-AzureRmServiceBusNamespaceKey</span></span>

## <span data-ttu-id="25f59-102">Sammanfattning</span><span class="sxs-lookup"><span data-stu-id="25f59-102">SYNOPSIS</span></span>
<span data-ttu-id="25f59-103">Hämtar primära och sekundära anslutnings strängar för namn området.</span><span class="sxs-lookup"><span data-stu-id="25f59-103">Gets the primary and secondary connection strings for the namespace.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="25f59-104">FRÅGESYNTAXEN</span><span class="sxs-lookup"><span data-stu-id="25f59-104">SYNTAX</span></span>

```
Get-AzureRmServiceBusNamespaceKey [-ResourceGroup] <String> -Namespace <String> -Name <String>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="25f59-105">PROBLEMBESKRIVNING</span><span class="sxs-lookup"><span data-stu-id="25f59-105">DESCRIPTION</span></span>
<span data-ttu-id="25f59-106">Cmdleten **Get-AzureRmServiceBusNamespaceKey** returnerar de primära och sekundära anslutnings strängarna för det angivna namn området.</span><span class="sxs-lookup"><span data-stu-id="25f59-106">The **Get-AzureRmServiceBusNamespaceKey** cmdlet returns the primary and secondary connection strings for the given namespace.</span></span> 

## <span data-ttu-id="25f59-107">BESKRIVS</span><span class="sxs-lookup"><span data-stu-id="25f59-107">EXAMPLES</span></span>

### <span data-ttu-id="25f59-108">Exempel 1</span><span class="sxs-lookup"><span data-stu-id="25f59-108">Example 1</span></span>
```
PS C:\> Get-AzureRmServiceBusNamespaceKey -ResourceGroup Default-ServiceBus-WestUS -NamespaceName SB-Example1 -AuthorizationRuleName AuthoRule1
```

<span data-ttu-id="25f59-109">Primära och sekundära anslutnings strängar till det angivna namn området.</span><span class="sxs-lookup"><span data-stu-id="25f59-109">Primary and secondary connection string to the specified namespace.</span></span>

## <span data-ttu-id="25f59-110">MALLPARAMETRAR</span><span class="sxs-lookup"><span data-stu-id="25f59-110">PARAMETERS</span></span>

### <span data-ttu-id="25f59-111">-ResourceGroup</span><span class="sxs-lookup"><span data-stu-id="25f59-111">-ResourceGroup</span></span>
<span data-ttu-id="25f59-112">Namnet på resurs gruppen.</span><span class="sxs-lookup"><span data-stu-id="25f59-112">The name of the resource group.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases: 

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="25f59-113">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="25f59-113">-DefaultProfile</span></span>
<span data-ttu-id="25f59-114">Autentiseringsuppgifter, konto, klient organisation och abonnemang som används för kommunikation med Azure.</span><span class="sxs-lookup"><span data-stu-id="25f59-114">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="25f59-115">-Namn</span><span class="sxs-lookup"><span data-stu-id="25f59-115">-Name</span></span>
<span data-ttu-id="25f59-116">Namn på ServiceBus namn område.</span><span class="sxs-lookup"><span data-stu-id="25f59-116">ServiceBus Namespace AuthorizationRule Name.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases: AuthorizationRuleName

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="25f59-117">-Namnrymd</span><span class="sxs-lookup"><span data-stu-id="25f59-117">-Namespace</span></span>
<span data-ttu-id="25f59-118">Namn områdes namnet ServiceBus.</span><span class="sxs-lookup"><span data-stu-id="25f59-118">ServiceBus Namespace Name.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases: NamespaceName

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="25f59-119">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="25f59-119">CommonParameters</span></span>
<span data-ttu-id="25f59-120">Den här cmdleten har stöd för de gemensamma parametrarna:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-disvariable,-utbuffer,-PipelineVariable,-verbose,-WarningAction och-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="25f59-120">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="25f59-121">Mer information finns i about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="25f59-121">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="25f59-122">KOSTNADS</span><span class="sxs-lookup"><span data-stu-id="25f59-122">INPUTS</span></span>

### <span data-ttu-id="25f59-123">-ResourceGroup</span><span class="sxs-lookup"><span data-stu-id="25f59-123">-ResourceGroup</span></span>
 <span data-ttu-id="25f59-124">System. String</span><span class="sxs-lookup"><span data-stu-id="25f59-124">System.String</span></span>
 

### <span data-ttu-id="25f59-125">-NamespaceName</span><span class="sxs-lookup"><span data-stu-id="25f59-125">-NamespaceName</span></span>
 <span data-ttu-id="25f59-126">System. String</span><span class="sxs-lookup"><span data-stu-id="25f59-126">System.String</span></span>
 

### <span data-ttu-id="25f59-127">-AuthorizationRuleName</span><span class="sxs-lookup"><span data-stu-id="25f59-127">-AuthorizationRuleName</span></span>
 <span data-ttu-id="25f59-128">System. String</span><span class="sxs-lookup"><span data-stu-id="25f59-128">System.String</span></span>

## <span data-ttu-id="25f59-129">VÄRDEN</span><span class="sxs-lookup"><span data-stu-id="25f59-129">OUTPUTS</span></span>

### <span data-ttu-id="25f59-130">Microsoft. Azure. Management. ServiceBus. Models. ResourceListKeys</span><span class="sxs-lookup"><span data-stu-id="25f59-130">Microsoft.Azure.Management.ServiceBus.Models.ResourceListKeys</span></span>
<span data-ttu-id="25f59-131">PrimaryConnectionString: slut punkt = SB://SB-example1.ServiceBus.Windows.net/; SharedAccessKeyName = AuthoRule1; SharedAccessKey = {SharedAccessKey värde} SecondaryConnectionString: slut punkt = SB://SB-example1.ServiceBus.Windows.net/; SharedAccessKeyName = AuthoRule1; SharedAccessKey = {SharedAccessKey värde} PrimaryKey: {PrimaryKey Value} SecondaryKey: {SecondaryKey värde} nyckel namn: AuthoRule1</span><span class="sxs-lookup"><span data-stu-id="25f59-131">PrimaryConnectionString   : Endpoint=sb://sb-example1.servicebus.windows.net/;SharedAccessKeyName=AuthoRule1;SharedAccessKey={SharedAccessKey value} SecondaryConnectionString : Endpoint=sb://sb-example1.servicebus.windows.net/;SharedAccessKeyName=AuthoRule1;SharedAccessKey={SharedAccessKey value} PrimaryKey                : {PrimaryKey value} SecondaryKey              : {SecondaryKey value} KeyName                   : AuthoRule1</span></span>

## <span data-ttu-id="25f59-132">ANMÄRKNINGAR</span><span class="sxs-lookup"><span data-stu-id="25f59-132">NOTES</span></span>

## <span data-ttu-id="25f59-133">RELATERADE LÄNKAR</span><span class="sxs-lookup"><span data-stu-id="25f59-133">RELATED LINKS</span></span>

