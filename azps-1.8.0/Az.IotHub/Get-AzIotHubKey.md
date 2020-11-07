---
external help file: Microsoft.Azure.PowerShell.Cmdlets.IotHub.dll-Help.xml
Module Name: Az.IotHub
online version: https://docs.microsoft.com/en-us/powershell/module/az.iothub/get-aziothubkey
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/IotHub/IotHub/help/Get-AzIotHubKey.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/IotHub/IotHub/help/Get-AzIotHubKey.md
ms.openlocfilehash: ac56d5392025a85d0310862a1786dde3d0f8ca2c
ms.sourcegitcommit: 4d2c178cd6df9151877b08d54c1f4a228dbec9d1
ms.translationtype: MT
ms.contentlocale: sv-SE
ms.lasthandoff: 01/29/2020
ms.locfileid: "93916470"
---
# <span data-ttu-id="fbc1e-101">Get-AzIotHubKey</span><span class="sxs-lookup"><span data-stu-id="fbc1e-101">Get-AzIotHubKey</span></span>

## <span data-ttu-id="fbc1e-102">Sammanfattning</span><span class="sxs-lookup"><span data-stu-id="fbc1e-102">SYNOPSIS</span></span>
<span data-ttu-id="fbc1e-103">Hämtar en IotHub-tangenten.</span><span class="sxs-lookup"><span data-stu-id="fbc1e-103">Gets an IotHub Key.</span></span>

## <span data-ttu-id="fbc1e-104">FRÅGESYNTAXEN</span><span class="sxs-lookup"><span data-stu-id="fbc1e-104">SYNTAX</span></span>

```
Get-AzIotHubKey [-ResourceGroupName] <String> [-Name] <String> [[-KeyName] <String>]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="fbc1e-105">PROBLEMBESKRIVNING</span><span class="sxs-lookup"><span data-stu-id="fbc1e-105">DESCRIPTION</span></span>
<span data-ttu-id="fbc1e-106">Hämtar en IotHub-tangenten.</span><span class="sxs-lookup"><span data-stu-id="fbc1e-106">Gets an IotHub Key.</span></span>
<span data-ttu-id="fbc1e-107">Du kan antingen lista alla knappar eller filtrera listan med ett specifikt nyckel namn.</span><span class="sxs-lookup"><span data-stu-id="fbc1e-107">You can either list all Keys or filter the list by a specific Key Name.</span></span>

## <span data-ttu-id="fbc1e-108">BESKRIVS</span><span class="sxs-lookup"><span data-stu-id="fbc1e-108">EXAMPLES</span></span>

### <span data-ttu-id="fbc1e-109">Exempel 1 Hämta alla knappar</span><span class="sxs-lookup"><span data-stu-id="fbc1e-109">Example 1 Get all Keys</span></span>
```
PS C:\> Get-AzIotHubKey -ResourceGroupName "myresourcegroup" -Name "myiothub"
```

<span data-ttu-id="fbc1e-110">Hämtar alla nycklar för IotHub med namnet "myiothub"</span><span class="sxs-lookup"><span data-stu-id="fbc1e-110">Gets all the Keys for the IotHub named "myiothub"</span></span>

### <span data-ttu-id="fbc1e-111">Exempel 2 Hämta information för en specifik nycklar</span><span class="sxs-lookup"><span data-stu-id="fbc1e-111">Example 2 Get information for a specific Key</span></span>
```
PS C:\> Get-AzIotHubKey -ResourceGroupName "myresourcegroup" -Name "myiothub" -KeyName "iothubowner"
```

<span data-ttu-id="fbc1e-112">Hämtar informationen för en nycklar med namnet "iothubowner" för IotHub med namnet "myiothub"</span><span class="sxs-lookup"><span data-stu-id="fbc1e-112">Gets the information for a key named "iothubowner" for the IotHub named "myiothub"</span></span>

## <span data-ttu-id="fbc1e-113">MALLPARAMETRAR</span><span class="sxs-lookup"><span data-stu-id="fbc1e-113">PARAMETERS</span></span>

### <span data-ttu-id="fbc1e-114">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="fbc1e-114">-DefaultProfile</span></span>
<span data-ttu-id="fbc1e-115">Autentiseringsuppgifter, konto, klient organisation och abonnemang som används för kommunikation med Azure</span><span class="sxs-lookup"><span data-stu-id="fbc1e-115">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="fbc1e-116">-Namn</span><span class="sxs-lookup"><span data-stu-id="fbc1e-116">-KeyName</span></span>
<span data-ttu-id="fbc1e-117">Namnet på tangenten</span><span class="sxs-lookup"><span data-stu-id="fbc1e-117">Name of the Key</span></span>

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

### <span data-ttu-id="fbc1e-118">-Namn</span><span class="sxs-lookup"><span data-stu-id="fbc1e-118">-Name</span></span>
<span data-ttu-id="fbc1e-119">Namn på IoT Hub.</span><span class="sxs-lookup"><span data-stu-id="fbc1e-119">Name of the IoT hub.</span></span> 

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

### <span data-ttu-id="fbc1e-120">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="fbc1e-120">-ResourceGroupName</span></span>
<span data-ttu-id="fbc1e-121">Resurs grupps namn</span><span class="sxs-lookup"><span data-stu-id="fbc1e-121">Resource Group Name</span></span>

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

### <span data-ttu-id="fbc1e-122">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="fbc1e-122">CommonParameters</span></span>
<span data-ttu-id="fbc1e-123">Den här cmdleten har stöd för de gemensamma parametrarna:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-disvariable,-utbuffer,-PipelineVariable,-verbose,-WarningAction och-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="fbc1e-123">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="fbc1e-124">Mer information finns i about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="fbc1e-124">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="fbc1e-125">KOSTNADS</span><span class="sxs-lookup"><span data-stu-id="fbc1e-125">INPUTS</span></span>

### <span data-ttu-id="fbc1e-126">System. String</span><span class="sxs-lookup"><span data-stu-id="fbc1e-126">System.String</span></span>

## <span data-ttu-id="fbc1e-127">VÄRDEN</span><span class="sxs-lookup"><span data-stu-id="fbc1e-127">OUTPUTS</span></span>

### <span data-ttu-id="fbc1e-128">Microsoft. Azure. commands. Management. IotHub. Models. PSSharedAccessSignatureAuthorizationRule</span><span class="sxs-lookup"><span data-stu-id="fbc1e-128">Microsoft.Azure.Commands.Management.IotHub.Models.PSSharedAccessSignatureAuthorizationRule</span></span>

## <span data-ttu-id="fbc1e-129">ANMÄRKNINGAR</span><span class="sxs-lookup"><span data-stu-id="fbc1e-129">NOTES</span></span>

## <span data-ttu-id="fbc1e-130">RELATERADE LÄNKAR</span><span class="sxs-lookup"><span data-stu-id="fbc1e-130">RELATED LINKS</span></span>
