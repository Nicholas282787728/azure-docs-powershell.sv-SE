---
external help file: Microsoft.Azure.Commands.IotHub.dll-Help.xml
Module Name: AzureRM.IotHub
online version: ''
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/IotHub/Commands.IotHub/help/Get-AzureRmIotHubKey.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/IotHub/Commands.IotHub/help/Get-AzureRmIotHubKey.md
ms.openlocfilehash: db2cf6c9daae5b96642a6408b990276feffc8598
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: sv-SE
ms.lasthandoff: 08/20/2020
ms.locfileid: "93582408"
---
# <span data-ttu-id="a5e9d-101">Get-AzureRmIotHubKey</span><span class="sxs-lookup"><span data-stu-id="a5e9d-101">Get-AzureRmIotHubKey</span></span>

## <span data-ttu-id="a5e9d-102">Sammanfattning</span><span class="sxs-lookup"><span data-stu-id="a5e9d-102">SYNOPSIS</span></span>
<span data-ttu-id="a5e9d-103">Hämtar en IotHub-tangenten.</span><span class="sxs-lookup"><span data-stu-id="a5e9d-103">Gets an IotHub Key.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="a5e9d-104">FRÅGESYNTAXEN</span><span class="sxs-lookup"><span data-stu-id="a5e9d-104">SYNTAX</span></span>

```
Get-AzureRmIotHubKey [-ResourceGroupName] <String> [-Name] <String> [[-KeyName] <String>]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="a5e9d-105">PROBLEMBESKRIVNING</span><span class="sxs-lookup"><span data-stu-id="a5e9d-105">DESCRIPTION</span></span>
<span data-ttu-id="a5e9d-106">Hämtar en IotHub-tangenten.</span><span class="sxs-lookup"><span data-stu-id="a5e9d-106">Gets an IotHub Key.</span></span>
<span data-ttu-id="a5e9d-107">Du kan antingen lista alla knappar eller filtrera listan med ett specifikt nyckel namn.</span><span class="sxs-lookup"><span data-stu-id="a5e9d-107">You can either list all Keys or filter the list by a specific Key Name.</span></span>

## <span data-ttu-id="a5e9d-108">BESKRIVS</span><span class="sxs-lookup"><span data-stu-id="a5e9d-108">EXAMPLES</span></span>

### <span data-ttu-id="a5e9d-109">Exempel 1 Hämta alla knappar</span><span class="sxs-lookup"><span data-stu-id="a5e9d-109">Example 1 Get all Keys</span></span>
```
PS C:\> Get-AzureRmIotHubKey -ResourceGroupName "myresourcegroup" -Name "myiothub"
```

<span data-ttu-id="a5e9d-110">Hämtar alla nycklar för IotHub med namnet "myiothub"</span><span class="sxs-lookup"><span data-stu-id="a5e9d-110">Gets all the Keys for the IotHub named "myiothub"</span></span>

### <span data-ttu-id="a5e9d-111">Exempel 2 Hämta information för en specifik nycklar</span><span class="sxs-lookup"><span data-stu-id="a5e9d-111">Example 2 Get information for a specific Key</span></span>
```
PS C:\> Get-AzureRmIotHubKey -ResourceGroupName "myresourcegroup" -Name "myiothub" -KeyName "iothubowner"
```

<span data-ttu-id="a5e9d-112">Hämtar informationen för en nycklar med namnet "iothubowner" för IotHub med namnet "myiothub"</span><span class="sxs-lookup"><span data-stu-id="a5e9d-112">Gets the information for a key named "iothubowner" for the IotHub named "myiothub"</span></span>

## <span data-ttu-id="a5e9d-113">MALLPARAMETRAR</span><span class="sxs-lookup"><span data-stu-id="a5e9d-113">PARAMETERS</span></span>

### <span data-ttu-id="a5e9d-114">-Namn</span><span class="sxs-lookup"><span data-stu-id="a5e9d-114">-KeyName</span></span>
<span data-ttu-id="a5e9d-115">Namnet på tangenten</span><span class="sxs-lookup"><span data-stu-id="a5e9d-115">Name of the Key</span></span>

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

### <span data-ttu-id="a5e9d-116">-Namn</span><span class="sxs-lookup"><span data-stu-id="a5e9d-116">-Name</span></span>
<span data-ttu-id="a5e9d-117">Namn på IoT Hub.</span><span class="sxs-lookup"><span data-stu-id="a5e9d-117">Name of the IoT hub.</span></span> 

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

### <span data-ttu-id="a5e9d-118">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="a5e9d-118">-ResourceGroupName</span></span>
<span data-ttu-id="a5e9d-119">Resurs grupps namn</span><span class="sxs-lookup"><span data-stu-id="a5e9d-119">Resource Group Name</span></span>

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

### <span data-ttu-id="a5e9d-120">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="a5e9d-120">-DefaultProfile</span></span>
<span data-ttu-id="a5e9d-121">Autentiseringsuppgifter, konto, klient organisation och abonnemang som används för kommunikation med Azure.</span><span class="sxs-lookup"><span data-stu-id="a5e9d-121">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="a5e9d-122">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="a5e9d-122">CommonParameters</span></span>
<span data-ttu-id="a5e9d-123">Den här cmdleten har stöd för de gemensamma parametrarna:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-disvariable,-utbuffer,-PipelineVariable,-verbose,-WarningAction och-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="a5e9d-123">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="a5e9d-124">Mer information finns i about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="a5e9d-124">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="a5e9d-125">KOSTNADS</span><span class="sxs-lookup"><span data-stu-id="a5e9d-125">INPUTS</span></span>

### <span data-ttu-id="a5e9d-126">System. String</span><span class="sxs-lookup"><span data-stu-id="a5e9d-126">System.String</span></span>

## <span data-ttu-id="a5e9d-127">VÄRDEN</span><span class="sxs-lookup"><span data-stu-id="a5e9d-127">OUTPUTS</span></span>

### <span data-ttu-id="a5e9d-128">Microsoft. Azure. commands. Management. IotHub. Models. PSSharedAccessSignatureAuthorizationRule</span><span class="sxs-lookup"><span data-stu-id="a5e9d-128">Microsoft.Azure.Commands.Management.IotHub.Models.PSSharedAccessSignatureAuthorizationRule</span></span>
<span data-ttu-id="a5e9d-129">System. Collections. Generic. list \` 1 \[ \[ Microsoft. Azure. kommandon. Management. IotHub. Models. PSSharedAccessSignatureAuthorizationRule, Microsoft. Azure. commands. IotHub, version = 1.0.0.0, Culture = neutralt, PublicKeyToken = null\]\]</span><span class="sxs-lookup"><span data-stu-id="a5e9d-129">System.Collections.Generic.List\`1\[\[Microsoft.Azure.Commands.Management.IotHub.Models.PSSharedAccessSignatureAuthorizationRule, Microsoft.Azure.Commands.IotHub, Version=1.0.0.0, Culture=neutral, PublicKeyToken=null\]\]</span></span>

## <span data-ttu-id="a5e9d-130">ANMÄRKNINGAR</span><span class="sxs-lookup"><span data-stu-id="a5e9d-130">NOTES</span></span>

## <span data-ttu-id="a5e9d-131">RELATERADE LÄNKAR</span><span class="sxs-lookup"><span data-stu-id="a5e9d-131">RELATED LINKS</span></span>
