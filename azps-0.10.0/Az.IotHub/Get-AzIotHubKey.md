---
external help file: Microsoft.Azure.PowerShell.Cmdlets.IotHub.dll-Help.xml
Module Name: Az.IotHub
online version: https://docs.microsoft.com/en-us/powershell/module/az.iothub/get-aziothubkey
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/Azs-tzl/src/IotHub/IotHub/help/Get-AzIotHubKey.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/Azs-tzl/src/IotHub/IotHub/help/Get-AzIotHubKey.md
ms.openlocfilehash: 29f9fc8847e4b8bf3ab348fcad8f312dab71fd0a
ms.sourcegitcommit: 4c61442a2df1cee633ce93cad9f6bc793803baa2
ms.translationtype: MT
ms.contentlocale: sv-SE
ms.lasthandoff: 04/16/2020
ms.locfileid: "93922813"
---
# <span data-ttu-id="e90a4-101">Get-AzIotHubKey</span><span class="sxs-lookup"><span data-stu-id="e90a4-101">Get-AzIotHubKey</span></span>

## <span data-ttu-id="e90a4-102">Sammanfattning</span><span class="sxs-lookup"><span data-stu-id="e90a4-102">SYNOPSIS</span></span>
<span data-ttu-id="e90a4-103">Hämtar en IotHub-tangenten.</span><span class="sxs-lookup"><span data-stu-id="e90a4-103">Gets an IotHub Key.</span></span>

## <span data-ttu-id="e90a4-104">FRÅGESYNTAXEN</span><span class="sxs-lookup"><span data-stu-id="e90a4-104">SYNTAX</span></span>

### <span data-ttu-id="e90a4-105">ResourceSet (standard)</span><span class="sxs-lookup"><span data-stu-id="e90a4-105">ResourceSet (Default)</span></span>
```
Get-AzIotHubKey [-ResourceGroupName] <String> [-Name] <String> [[-KeyName] <String>]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="e90a4-106">ResourceIdSet</span><span class="sxs-lookup"><span data-stu-id="e90a4-106">ResourceIdSet</span></span>
```
Get-AzIotHubKey [-HubId] <String> [[-KeyName] <String>] [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

## <span data-ttu-id="e90a4-107">PROBLEMBESKRIVNING</span><span class="sxs-lookup"><span data-stu-id="e90a4-107">DESCRIPTION</span></span>
<span data-ttu-id="e90a4-108">Hämtar en IotHub-tangenten.</span><span class="sxs-lookup"><span data-stu-id="e90a4-108">Gets an IotHub Key.</span></span>
<span data-ttu-id="e90a4-109">Du kan antingen lista alla knappar eller filtrera listan med ett specifikt nyckel namn.</span><span class="sxs-lookup"><span data-stu-id="e90a4-109">You can either list all Keys or filter the list by a specific Key Name.</span></span>

## <span data-ttu-id="e90a4-110">BESKRIVS</span><span class="sxs-lookup"><span data-stu-id="e90a4-110">EXAMPLES</span></span>

### <span data-ttu-id="e90a4-111">Exempel 1 Hämta alla knappar</span><span class="sxs-lookup"><span data-stu-id="e90a4-111">Example 1 Get all Keys</span></span>
```
PS C:\> Get-AzIotHubKey -ResourceGroupName "myresourcegroup" -Name "myiothub"
```

<span data-ttu-id="e90a4-112">Hämtar alla nycklar för IotHub med namnet "myiothub"</span><span class="sxs-lookup"><span data-stu-id="e90a4-112">Gets all the Keys for the IotHub named "myiothub"</span></span>

### <span data-ttu-id="e90a4-113">Exempel 2 Hämta information för en specifik nycklar</span><span class="sxs-lookup"><span data-stu-id="e90a4-113">Example 2 Get information for a specific Key</span></span>
```
PS C:\> Get-AzIotHubKey -ResourceGroupName "myresourcegroup" -Name "myiothub" -KeyName "iothubowner"
```

<span data-ttu-id="e90a4-114">Hämtar informationen för en nycklar med namnet "iothubowner" för IotHub med namnet "myiothub"</span><span class="sxs-lookup"><span data-stu-id="e90a4-114">Gets the information for a key named "iothubowner" for the IotHub named "myiothub"</span></span>

## <span data-ttu-id="e90a4-115">MALLPARAMETRAR</span><span class="sxs-lookup"><span data-stu-id="e90a4-115">PARAMETERS</span></span>

### <span data-ttu-id="e90a4-116">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="e90a4-116">-DefaultProfile</span></span>
<span data-ttu-id="e90a4-117">Autentiseringsuppgifter, konto, klient organisation och abonnemang som används för kommunikation med Azure</span><span class="sxs-lookup"><span data-stu-id="e90a4-117">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="e90a4-118">-HubId</span><span class="sxs-lookup"><span data-stu-id="e90a4-118">-HubId</span></span>
<span data-ttu-id="e90a4-119">Resurs-ID för IotHub</span><span class="sxs-lookup"><span data-stu-id="e90a4-119">IotHub Resource Id</span></span>

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

### <span data-ttu-id="e90a4-120">-Namn</span><span class="sxs-lookup"><span data-stu-id="e90a4-120">-KeyName</span></span>
<span data-ttu-id="e90a4-121">Namnet på tangenten</span><span class="sxs-lookup"><span data-stu-id="e90a4-121">Name of the Key</span></span>

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

### <span data-ttu-id="e90a4-122">-Namn</span><span class="sxs-lookup"><span data-stu-id="e90a4-122">-Name</span></span>
<span data-ttu-id="e90a4-123">Namn på IoT Hub.</span><span class="sxs-lookup"><span data-stu-id="e90a4-123">Name of the IoT hub.</span></span> 

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

### <span data-ttu-id="e90a4-124">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="e90a4-124">-ResourceGroupName</span></span>
<span data-ttu-id="e90a4-125">Resurs grupps namn</span><span class="sxs-lookup"><span data-stu-id="e90a4-125">Resource Group Name</span></span>

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

### <span data-ttu-id="e90a4-126">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="e90a4-126">CommonParameters</span></span>
<span data-ttu-id="e90a4-127">Den här cmdleten har stöd för de gemensamma parametrarna:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-disvariable,-utbuffer,-PipelineVariable,-verbose,-WarningAction och-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="e90a4-127">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="e90a4-128">Mer information finns i about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="e90a4-128">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="e90a4-129">KOSTNADS</span><span class="sxs-lookup"><span data-stu-id="e90a4-129">INPUTS</span></span>

### <span data-ttu-id="e90a4-130">System. String</span><span class="sxs-lookup"><span data-stu-id="e90a4-130">System.String</span></span>

## <span data-ttu-id="e90a4-131">VÄRDEN</span><span class="sxs-lookup"><span data-stu-id="e90a4-131">OUTPUTS</span></span>

### <span data-ttu-id="e90a4-132">Microsoft. Azure. commands. Management. IotHub. Models. PSSharedAccessSignatureAuthorizationRule</span><span class="sxs-lookup"><span data-stu-id="e90a4-132">Microsoft.Azure.Commands.Management.IotHub.Models.PSSharedAccessSignatureAuthorizationRule</span></span>

## <span data-ttu-id="e90a4-133">ANMÄRKNINGAR</span><span class="sxs-lookup"><span data-stu-id="e90a4-133">NOTES</span></span>

## <span data-ttu-id="e90a4-134">RELATERADE LÄNKAR</span><span class="sxs-lookup"><span data-stu-id="e90a4-134">RELATED LINKS</span></span>
