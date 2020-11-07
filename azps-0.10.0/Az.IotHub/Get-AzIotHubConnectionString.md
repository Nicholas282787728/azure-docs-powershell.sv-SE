---
external help file: Microsoft.Azure.PowerShell.Cmdlets.IotHub.dll-Help.xml
Module Name: Az.IotHub
online version: https://docs.microsoft.com/en-us/powershell/module/az.iothub/get-aziothubconnectionstring
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/Azs-tzl/src/IotHub/IotHub/help/Get-AzIotHubConnectionString.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/Azs-tzl/src/IotHub/IotHub/help/Get-AzIotHubConnectionString.md
ms.openlocfilehash: 92d1e3f2ef1ba87a5e9683f7ac6617e31bb8a055
ms.sourcegitcommit: 4c61442a2df1cee633ce93cad9f6bc793803baa2
ms.translationtype: MT
ms.contentlocale: sv-SE
ms.lasthandoff: 04/16/2020
ms.locfileid: "93922822"
---
# <span data-ttu-id="12705-101">Get-AzIotHubConnectionString</span><span class="sxs-lookup"><span data-stu-id="12705-101">Get-AzIotHubConnectionString</span></span>

## <span data-ttu-id="12705-102">Sammanfattning</span><span class="sxs-lookup"><span data-stu-id="12705-102">SYNOPSIS</span></span>
<span data-ttu-id="12705-103">Hämtar IotHub-connectionstringna.</span><span class="sxs-lookup"><span data-stu-id="12705-103">Gets the IotHub connectionstrings.</span></span>

## <span data-ttu-id="12705-104">FRÅGESYNTAXEN</span><span class="sxs-lookup"><span data-stu-id="12705-104">SYNTAX</span></span>

```
Get-AzIotHubConnectionString [-ResourceGroupName] <String> [-Name] <String> [[-KeyName] <String>]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="12705-105">PROBLEMBESKRIVNING</span><span class="sxs-lookup"><span data-stu-id="12705-105">DESCRIPTION</span></span>
<span data-ttu-id="12705-106">Hämtar IotHub-connectionstringna.</span><span class="sxs-lookup"><span data-stu-id="12705-106">Gets the IotHub connectionstrings.</span></span>
<span data-ttu-id="12705-107">Du kan antingen skaffa ConnectionString för alla nycklar eller filtrera dem med ett specifikt nyckel namn.</span><span class="sxs-lookup"><span data-stu-id="12705-107">You can either get connectionstrings for all the keys or filter them by a specific key name.</span></span>

## <span data-ttu-id="12705-108">BESKRIVS</span><span class="sxs-lookup"><span data-stu-id="12705-108">EXAMPLES</span></span>

### <span data-ttu-id="12705-109">Exempel 1 Hämta alla IotHub-ConnectionString</span><span class="sxs-lookup"><span data-stu-id="12705-109">Example 1 Get All IotHub connectionstrings</span></span>
```
PS C:\> Get-AzIotHubConnectionString -ResourceGroupName "myresourcegroup" -Name "myiothub"
```

<span data-ttu-id="12705-110">Hämtar ConnectionString för alla nycklar för iothub med namnet "myiothub"</span><span class="sxs-lookup"><span data-stu-id="12705-110">Gets the connectionstrings for all keys for the iothub named "myiothub"</span></span>

### <span data-ttu-id="12705-111">Exempel 2 Hämta IotHub-ConnectionString för en specifik-tangenten</span><span class="sxs-lookup"><span data-stu-id="12705-111">Example 2 Get the IotHub connectionstrings for a specific key</span></span>
```
PS C:\> Get-AzIotHubConnectionString -ResourceGroupName "myresourcegroup" -Name "myiothub" -KeyName "mykey"
```

<span data-ttu-id="12705-112">Hämtar connectionstringna för tangenten med namnet "MyKey" för iothub med namnet "myiothub"</span><span class="sxs-lookup"><span data-stu-id="12705-112">Gets the connectionstrings for the key named "mykey" for the iothub named "myiothub"</span></span>

## <span data-ttu-id="12705-113">MALLPARAMETRAR</span><span class="sxs-lookup"><span data-stu-id="12705-113">PARAMETERS</span></span>

### <span data-ttu-id="12705-114">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="12705-114">-DefaultProfile</span></span>
<span data-ttu-id="12705-115">Autentiseringsuppgifter, konto, klient organisation och abonnemang som används för kommunikation med Azure</span><span class="sxs-lookup"><span data-stu-id="12705-115">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="12705-116">-Namn</span><span class="sxs-lookup"><span data-stu-id="12705-116">-KeyName</span></span>
<span data-ttu-id="12705-117">Namnet på tangenten</span><span class="sxs-lookup"><span data-stu-id="12705-117">Name of the Key</span></span>

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

### <span data-ttu-id="12705-118">-Namn</span><span class="sxs-lookup"><span data-stu-id="12705-118">-Name</span></span>
<span data-ttu-id="12705-119">Namn på IotHub</span><span class="sxs-lookup"><span data-stu-id="12705-119">Name of the IotHub</span></span>

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

### <span data-ttu-id="12705-120">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="12705-120">-ResourceGroupName</span></span>
<span data-ttu-id="12705-121">Resurs grupps namn</span><span class="sxs-lookup"><span data-stu-id="12705-121">Resource Group Name</span></span>

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

### <span data-ttu-id="12705-122">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="12705-122">CommonParameters</span></span>
<span data-ttu-id="12705-123">Den här cmdleten har stöd för de gemensamma parametrarna:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-disvariable,-utbuffer,-PipelineVariable,-verbose,-WarningAction och-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="12705-123">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="12705-124">Mer information finns i about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="12705-124">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="12705-125">KOSTNADS</span><span class="sxs-lookup"><span data-stu-id="12705-125">INPUTS</span></span>

### <span data-ttu-id="12705-126">System. String</span><span class="sxs-lookup"><span data-stu-id="12705-126">System.String</span></span>

## <span data-ttu-id="12705-127">VÄRDEN</span><span class="sxs-lookup"><span data-stu-id="12705-127">OUTPUTS</span></span>

### <span data-ttu-id="12705-128">Microsoft. Azure. commands. Management. IotHub. Models. PSSharedAccessSignatureAuthorizationRule</span><span class="sxs-lookup"><span data-stu-id="12705-128">Microsoft.Azure.Commands.Management.IotHub.Models.PSSharedAccessSignatureAuthorizationRule</span></span>

## <span data-ttu-id="12705-129">ANMÄRKNINGAR</span><span class="sxs-lookup"><span data-stu-id="12705-129">NOTES</span></span>

## <span data-ttu-id="12705-130">RELATERADE LÄNKAR</span><span class="sxs-lookup"><span data-stu-id="12705-130">RELATED LINKS</span></span>
