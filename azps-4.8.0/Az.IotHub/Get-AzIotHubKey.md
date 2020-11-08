---
external help file: Microsoft.Azure.PowerShell.Cmdlets.IotHub.dll-Help.xml
Module Name: Az.IotHub
online version: https://docs.microsoft.com/en-us/powershell/module/az.iothub/get-aziothubkey
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/IotHub/IotHub/help/Get-AzIotHubKey.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/IotHub/IotHub/help/Get-AzIotHubKey.md
ms.openlocfilehash: 258d1e1bad9eca1fd8817e1eaa499eb5bc3d8d49
ms.sourcegitcommit: 1de2b6c3c99197958fa2101bc37680e7507f91ac
ms.translationtype: MT
ms.contentlocale: sv-SE
ms.lasthandoff: 10/13/2020
ms.locfileid: "94262647"
---
# <span data-ttu-id="900dc-101">Get-AzIotHubKey</span><span class="sxs-lookup"><span data-stu-id="900dc-101">Get-AzIotHubKey</span></span>

## <span data-ttu-id="900dc-102">Sammanfattning</span><span class="sxs-lookup"><span data-stu-id="900dc-102">SYNOPSIS</span></span>
<span data-ttu-id="900dc-103">Hämtar en IotHub-tangenten.</span><span class="sxs-lookup"><span data-stu-id="900dc-103">Gets an IotHub Key.</span></span>

## <span data-ttu-id="900dc-104">FRÅGESYNTAXEN</span><span class="sxs-lookup"><span data-stu-id="900dc-104">SYNTAX</span></span>

### <span data-ttu-id="900dc-105">ResourceSet (standard)</span><span class="sxs-lookup"><span data-stu-id="900dc-105">ResourceSet (Default)</span></span>
```
Get-AzIotHubKey [-ResourceGroupName] <String> [-Name] <String> [[-KeyName] <String>]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="900dc-106">ResourceIdSet</span><span class="sxs-lookup"><span data-stu-id="900dc-106">ResourceIdSet</span></span>
```
Get-AzIotHubKey [-HubId] <String> [[-KeyName] <String>] [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

## <span data-ttu-id="900dc-107">PROBLEMBESKRIVNING</span><span class="sxs-lookup"><span data-stu-id="900dc-107">DESCRIPTION</span></span>
<span data-ttu-id="900dc-108">Hämtar en IotHub-tangenten.</span><span class="sxs-lookup"><span data-stu-id="900dc-108">Gets an IotHub Key.</span></span>
<span data-ttu-id="900dc-109">Du kan antingen lista alla knappar eller filtrera listan med ett specifikt nyckel namn.</span><span class="sxs-lookup"><span data-stu-id="900dc-109">You can either list all Keys or filter the list by a specific Key Name.</span></span>

## <span data-ttu-id="900dc-110">BESKRIVS</span><span class="sxs-lookup"><span data-stu-id="900dc-110">EXAMPLES</span></span>

### <span data-ttu-id="900dc-111">Exempel 1 Hämta alla knappar</span><span class="sxs-lookup"><span data-stu-id="900dc-111">Example 1 Get all Keys</span></span>
```
PS C:\> Get-AzIotHubKey -ResourceGroupName "myresourcegroup" -Name "myiothub"
```

<span data-ttu-id="900dc-112">Hämtar alla nycklar för IotHub med namnet "myiothub"</span><span class="sxs-lookup"><span data-stu-id="900dc-112">Gets all the Keys for the IotHub named "myiothub"</span></span>

### <span data-ttu-id="900dc-113">Exempel 2 Hämta information för en specifik nycklar</span><span class="sxs-lookup"><span data-stu-id="900dc-113">Example 2 Get information for a specific Key</span></span>
```
PS C:\> Get-AzIotHubKey -ResourceGroupName "myresourcegroup" -Name "myiothub" -KeyName "iothubowner"
```

<span data-ttu-id="900dc-114">Hämtar informationen för en nycklar med namnet "iothubowner" för IotHub med namnet "myiothub"</span><span class="sxs-lookup"><span data-stu-id="900dc-114">Gets the information for a key named "iothubowner" for the IotHub named "myiothub"</span></span>

## <span data-ttu-id="900dc-115">MALLPARAMETRAR</span><span class="sxs-lookup"><span data-stu-id="900dc-115">PARAMETERS</span></span>

### <span data-ttu-id="900dc-116">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="900dc-116">-DefaultProfile</span></span>
<span data-ttu-id="900dc-117">Autentiseringsuppgifter, konto, klient organisation och abonnemang som används för kommunikation med Azure</span><span class="sxs-lookup"><span data-stu-id="900dc-117">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="900dc-118">-HubId</span><span class="sxs-lookup"><span data-stu-id="900dc-118">-HubId</span></span>
<span data-ttu-id="900dc-119">Resurs-ID för IotHub</span><span class="sxs-lookup"><span data-stu-id="900dc-119">IotHub Resource Id</span></span>

```yaml
Type: System.String
Parameter Sets: ResourceIdSet
Aliases:

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="900dc-120">-Namn</span><span class="sxs-lookup"><span data-stu-id="900dc-120">-KeyName</span></span>
<span data-ttu-id="900dc-121">Namnet på tangenten</span><span class="sxs-lookup"><span data-stu-id="900dc-121">Name of the Key</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: False
Position: 1
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="900dc-122">-Namn</span><span class="sxs-lookup"><span data-stu-id="900dc-122">-Name</span></span>
<span data-ttu-id="900dc-123">Namn på IoT Hub.</span><span class="sxs-lookup"><span data-stu-id="900dc-123">Name of the IoT hub.</span></span> 

```yaml
Type: System.String
Parameter Sets: ResourceSet
Aliases:

Required: True
Position: 1
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="900dc-124">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="900dc-124">-ResourceGroupName</span></span>
<span data-ttu-id="900dc-125">Resurs grupps namn</span><span class="sxs-lookup"><span data-stu-id="900dc-125">Resource Group Name</span></span>

```yaml
Type: System.String
Parameter Sets: ResourceSet
Aliases:

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="900dc-126">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="900dc-126">CommonParameters</span></span>
<span data-ttu-id="900dc-127">Den här cmdleten har stöd för de gemensamma parametrarna:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-disvariable,-utbuffer,-PipelineVariable,-verbose,-WarningAction och-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="900dc-127">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="900dc-128">Mer information finns i about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="900dc-128">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="900dc-129">KOSTNADS</span><span class="sxs-lookup"><span data-stu-id="900dc-129">INPUTS</span></span>

### <span data-ttu-id="900dc-130">System. String</span><span class="sxs-lookup"><span data-stu-id="900dc-130">System.String</span></span>

## <span data-ttu-id="900dc-131">VÄRDEN</span><span class="sxs-lookup"><span data-stu-id="900dc-131">OUTPUTS</span></span>

### <span data-ttu-id="900dc-132">Microsoft. Azure. commands. Management. IotHub. Models. PSSharedAccessSignatureAuthorizationRule</span><span class="sxs-lookup"><span data-stu-id="900dc-132">Microsoft.Azure.Commands.Management.IotHub.Models.PSSharedAccessSignatureAuthorizationRule</span></span>

## <span data-ttu-id="900dc-133">ANMÄRKNINGAR</span><span class="sxs-lookup"><span data-stu-id="900dc-133">NOTES</span></span>

## <span data-ttu-id="900dc-134">RELATERADE LÄNKAR</span><span class="sxs-lookup"><span data-stu-id="900dc-134">RELATED LINKS</span></span>
