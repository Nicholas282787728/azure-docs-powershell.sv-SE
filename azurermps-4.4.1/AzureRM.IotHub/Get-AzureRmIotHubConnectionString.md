---
external help file: Microsoft.Azure.Commands.IotHub.dll-Help.xml
Module Name: AzureRM.IotHub
online version: ''
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/IotHub/Commands.IotHub/help/Get-AzureRmIotHubConnectionString.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/IotHub/Commands.IotHub/help/Get-AzureRmIotHubConnectionString.md
ms.openlocfilehash: 52c5bee4e699ff063794f140ce4360669180a164
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: sv-SE
ms.lasthandoff: 08/20/2020
ms.locfileid: "93756957"
---
# <span data-ttu-id="2ee15-101">Get-AzureRmIotHubConnectionString</span><span class="sxs-lookup"><span data-stu-id="2ee15-101">Get-AzureRmIotHubConnectionString</span></span>

## <span data-ttu-id="2ee15-102">Sammanfattning</span><span class="sxs-lookup"><span data-stu-id="2ee15-102">SYNOPSIS</span></span>
<span data-ttu-id="2ee15-103">Hämtar IotHub-connectionstringna.</span><span class="sxs-lookup"><span data-stu-id="2ee15-103">Gets the IotHub connectionstrings.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="2ee15-104">FRÅGESYNTAXEN</span><span class="sxs-lookup"><span data-stu-id="2ee15-104">SYNTAX</span></span>

```
Get-AzureRmIotHubConnectionString [-ResourceGroupName] <String> [-Name] <String> [[-KeyName] <String>]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="2ee15-105">PROBLEMBESKRIVNING</span><span class="sxs-lookup"><span data-stu-id="2ee15-105">DESCRIPTION</span></span>
<span data-ttu-id="2ee15-106">Hämtar IotHub-connectionstringna.</span><span class="sxs-lookup"><span data-stu-id="2ee15-106">Gets the IotHub connectionstrings.</span></span>
<span data-ttu-id="2ee15-107">Du kan antingen skaffa ConnectionString för alla nycklar eller filtrera dem med ett specifikt nyckel namn.</span><span class="sxs-lookup"><span data-stu-id="2ee15-107">You can either get connectionstrings for all the keys or filter them by a specific key name.</span></span>

## <span data-ttu-id="2ee15-108">BESKRIVS</span><span class="sxs-lookup"><span data-stu-id="2ee15-108">EXAMPLES</span></span>

### <span data-ttu-id="2ee15-109">Exempel 1 Hämta alla IotHub-ConnectionString</span><span class="sxs-lookup"><span data-stu-id="2ee15-109">Example 1 Get All IotHub connectionstrings</span></span>
```
PS C:\> Get-AzureRmIotHubConnectionString -ResourceGroupName "myresourcegroup" -Name "myiothub"
```

<span data-ttu-id="2ee15-110">Hämtar ConnectionString för alla nycklar för iothub med namnet "myiothub"</span><span class="sxs-lookup"><span data-stu-id="2ee15-110">Gets the connectionstrings for all keys for the iothub named "myiothub"</span></span>

### <span data-ttu-id="2ee15-111">Exempel 2 Hämta IotHub-ConnectionString för en specifik-tangenten</span><span class="sxs-lookup"><span data-stu-id="2ee15-111">Example 2 Get the IotHub connectionstrings for a specific key</span></span>
```
PS C:\> Get-AzureRmIotHubConnectionString -ResourceGroupName "myresourcegroup" -Name "myiothub" -KeyName "mykey"
```

<span data-ttu-id="2ee15-112">Hämtar connectionstringna för tangenten med namnet "MyKey" för iothub med namnet "myiothub"</span><span class="sxs-lookup"><span data-stu-id="2ee15-112">Gets the connectionstrings for the key named "mykey" for the iothub named "myiothub"</span></span>

## <span data-ttu-id="2ee15-113">MALLPARAMETRAR</span><span class="sxs-lookup"><span data-stu-id="2ee15-113">PARAMETERS</span></span>

### <span data-ttu-id="2ee15-114">-Namn</span><span class="sxs-lookup"><span data-stu-id="2ee15-114">-KeyName</span></span>
<span data-ttu-id="2ee15-115">Namnet på tangenten</span><span class="sxs-lookup"><span data-stu-id="2ee15-115">Name of the Key</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases: 

Required: False
Position: 2
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="2ee15-116">-Namn</span><span class="sxs-lookup"><span data-stu-id="2ee15-116">-Name</span></span>
<span data-ttu-id="2ee15-117">Namn på IotHub</span><span class="sxs-lookup"><span data-stu-id="2ee15-117">Name of the IotHub</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases: 

Required: True
Position: 1
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="2ee15-118">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="2ee15-118">-ResourceGroupName</span></span>
<span data-ttu-id="2ee15-119">Resurs grupps namn</span><span class="sxs-lookup"><span data-stu-id="2ee15-119">Resource Group Name</span></span>

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

### <span data-ttu-id="2ee15-120">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="2ee15-120">-DefaultProfile</span></span>
<span data-ttu-id="2ee15-121">Autentiseringsuppgifter, konto, klient organisation och abonnemang som används för kommunikation med Azure.</span><span class="sxs-lookup"><span data-stu-id="2ee15-121">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="2ee15-122">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="2ee15-122">CommonParameters</span></span>
<span data-ttu-id="2ee15-123">Den här cmdleten har stöd för de gemensamma parametrarna:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-disvariable,-utbuffer,-PipelineVariable,-verbose,-WarningAction och-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="2ee15-123">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="2ee15-124">Mer information finns i about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="2ee15-124">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="2ee15-125">KOSTNADS</span><span class="sxs-lookup"><span data-stu-id="2ee15-125">INPUTS</span></span>

### <span data-ttu-id="2ee15-126">System. String</span><span class="sxs-lookup"><span data-stu-id="2ee15-126">System.String</span></span>

## <span data-ttu-id="2ee15-127">VÄRDEN</span><span class="sxs-lookup"><span data-stu-id="2ee15-127">OUTPUTS</span></span>

### <span data-ttu-id="2ee15-128">Microsoft. Azure. commands. Management. IotHub. Models. PSSharedAccessSignatureAuthorizationRule</span><span class="sxs-lookup"><span data-stu-id="2ee15-128">Microsoft.Azure.Commands.Management.IotHub.Models.PSSharedAccessSignatureAuthorizationRule</span></span>
<span data-ttu-id="2ee15-129">System. Collections. Generic. list \` 1 \[ \[ Microsoft. Azure. kommandon. Management. IotHub. Models. PSSharedAccessSignatureAuthorizationRule, Microsoft. Azure. commands. IotHub, version = 1.0.0.0, Culture = neutralt, PublicKeyToken = null\]\]</span><span class="sxs-lookup"><span data-stu-id="2ee15-129">System.Collections.Generic.List\`1\[\[Microsoft.Azure.Commands.Management.IotHub.Models.PSSharedAccessSignatureAuthorizationRule, Microsoft.Azure.Commands.IotHub, Version=1.0.0.0, Culture=neutral, PublicKeyToken=null\]\]</span></span>

## <span data-ttu-id="2ee15-130">ANMÄRKNINGAR</span><span class="sxs-lookup"><span data-stu-id="2ee15-130">NOTES</span></span>

## <span data-ttu-id="2ee15-131">RELATERADE LÄNKAR</span><span class="sxs-lookup"><span data-stu-id="2ee15-131">RELATED LINKS</span></span>

