---
external help file: Microsoft.Azure.PowerShell.Cmdlets.IotHub.dll-Help.xml
Module Name: Az.IotHub
online version: https://docs.microsoft.com/en-us/powershell/module/az.iothub/get-aziothubconnectionstring
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/IotHub/IotHub/help/Get-AzIotHubConnectionString.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/IotHub/IotHub/help/Get-AzIotHubConnectionString.md
ms.openlocfilehash: f84d233280bc771b90f47c5769fdb6d3f35c2e0c
ms.sourcegitcommit: b4a38bcb0501a9016a4998efd377aa75d3ef9ce8
ms.translationtype: MT
ms.contentlocale: sv-SE
ms.lasthandoff: 10/27/2020
ms.locfileid: "94270987"
---
# <span data-ttu-id="0f235-101">Get-AzIotHubConnectionString</span><span class="sxs-lookup"><span data-stu-id="0f235-101">Get-AzIotHubConnectionString</span></span>

## <span data-ttu-id="0f235-102">Sammanfattning</span><span class="sxs-lookup"><span data-stu-id="0f235-102">SYNOPSIS</span></span>
<span data-ttu-id="0f235-103">Hämtar IotHub-connectionstringna.</span><span class="sxs-lookup"><span data-stu-id="0f235-103">Gets the IotHub connectionstrings.</span></span>

## <span data-ttu-id="0f235-104">FRÅGESYNTAXEN</span><span class="sxs-lookup"><span data-stu-id="0f235-104">SYNTAX</span></span>

```
Get-AzIotHubConnectionString [-ResourceGroupName] <String> [-Name] <String> [[-KeyName] <String>]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="0f235-105">PROBLEMBESKRIVNING</span><span class="sxs-lookup"><span data-stu-id="0f235-105">DESCRIPTION</span></span>
<span data-ttu-id="0f235-106">Hämtar IotHub-connectionstringna.</span><span class="sxs-lookup"><span data-stu-id="0f235-106">Gets the IotHub connectionstrings.</span></span>
<span data-ttu-id="0f235-107">Du kan antingen skaffa ConnectionString för alla nycklar eller filtrera dem med ett specifikt nyckel namn.</span><span class="sxs-lookup"><span data-stu-id="0f235-107">You can either get connectionstrings for all the keys or filter them by a specific key name.</span></span>

## <span data-ttu-id="0f235-108">BESKRIVS</span><span class="sxs-lookup"><span data-stu-id="0f235-108">EXAMPLES</span></span>

### <span data-ttu-id="0f235-109">Exempel 1 Hämta alla IotHub-ConnectionString</span><span class="sxs-lookup"><span data-stu-id="0f235-109">Example 1 Get All IotHub connectionstrings</span></span>
```
PS C:\> Get-AzIotHubConnectionString -ResourceGroupName "myresourcegroup" -Name "myiothub"
```

<span data-ttu-id="0f235-110">Hämtar ConnectionString för alla nycklar för iothub med namnet "myiothub"</span><span class="sxs-lookup"><span data-stu-id="0f235-110">Gets the connectionstrings for all keys for the iothub named "myiothub"</span></span>

### <span data-ttu-id="0f235-111">Exempel 2 Hämta IotHub-ConnectionString för en specifik-tangenten</span><span class="sxs-lookup"><span data-stu-id="0f235-111">Example 2 Get the IotHub connectionstrings for a specific key</span></span>
```
PS C:\> Get-AzIotHubConnectionString -ResourceGroupName "myresourcegroup" -Name "myiothub" -KeyName "mykey"
```

<span data-ttu-id="0f235-112">Hämtar connectionstringna för tangenten med namnet "MyKey" för iothub med namnet "myiothub"</span><span class="sxs-lookup"><span data-stu-id="0f235-112">Gets the connectionstrings for the key named "mykey" for the iothub named "myiothub"</span></span>

## <span data-ttu-id="0f235-113">MALLPARAMETRAR</span><span class="sxs-lookup"><span data-stu-id="0f235-113">PARAMETERS</span></span>

### <span data-ttu-id="0f235-114">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="0f235-114">-DefaultProfile</span></span>
<span data-ttu-id="0f235-115">Autentiseringsuppgifter, konto, klient organisation och abonnemang som används för kommunikation med Azure</span><span class="sxs-lookup"><span data-stu-id="0f235-115">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="0f235-116">-Namn</span><span class="sxs-lookup"><span data-stu-id="0f235-116">-KeyName</span></span>
<span data-ttu-id="0f235-117">Namnet på tangenten</span><span class="sxs-lookup"><span data-stu-id="0f235-117">Name of the Key</span></span>

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

### <span data-ttu-id="0f235-118">-Namn</span><span class="sxs-lookup"><span data-stu-id="0f235-118">-Name</span></span>
<span data-ttu-id="0f235-119">Namn på IotHub</span><span class="sxs-lookup"><span data-stu-id="0f235-119">Name of the IotHub</span></span>

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

### <span data-ttu-id="0f235-120">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="0f235-120">-ResourceGroupName</span></span>
<span data-ttu-id="0f235-121">Resurs grupps namn</span><span class="sxs-lookup"><span data-stu-id="0f235-121">Resource Group Name</span></span>

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

### <span data-ttu-id="0f235-122">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="0f235-122">CommonParameters</span></span>
<span data-ttu-id="0f235-123">Den här cmdleten har stöd för de gemensamma parametrarna:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-disvariable,-utbuffer,-PipelineVariable,-verbose,-WarningAction och-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="0f235-123">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="0f235-124">Mer information finns i about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="0f235-124">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="0f235-125">KOSTNADS</span><span class="sxs-lookup"><span data-stu-id="0f235-125">INPUTS</span></span>

### <span data-ttu-id="0f235-126">System. String</span><span class="sxs-lookup"><span data-stu-id="0f235-126">System.String</span></span>

## <span data-ttu-id="0f235-127">VÄRDEN</span><span class="sxs-lookup"><span data-stu-id="0f235-127">OUTPUTS</span></span>

### <span data-ttu-id="0f235-128">Microsoft. Azure. commands. Management. IotHub. Models. PSSharedAccessSignatureAuthorizationRule</span><span class="sxs-lookup"><span data-stu-id="0f235-128">Microsoft.Azure.Commands.Management.IotHub.Models.PSSharedAccessSignatureAuthorizationRule</span></span>

## <span data-ttu-id="0f235-129">ANMÄRKNINGAR</span><span class="sxs-lookup"><span data-stu-id="0f235-129">NOTES</span></span>

## <span data-ttu-id="0f235-130">RELATERADE LÄNKAR</span><span class="sxs-lookup"><span data-stu-id="0f235-130">RELATED LINKS</span></span>