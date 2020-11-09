---
external help file: Microsoft.Azure.PowerShell.Cmdlets.SignalR.dll-Help.xml
Module Name: Az.SignalR
online version: https://docs.microsoft.com/en-us/powershell/module/az.signalr/test-azsignalrname
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/SignalR/SignalR/help/Test-AzSignalRName.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/SignalR/SignalR/help/Test-AzSignalRName.md
ms.openlocfilehash: b00a408df2fe1705309152a02484d3b18ea41e9e
ms.sourcegitcommit: b4a38bcb0501a9016a4998efd377aa75d3ef9ce8
ms.translationtype: MT
ms.contentlocale: sv-SE
ms.lasthandoff: 10/27/2020
ms.locfileid: "94324215"
---
# <span data-ttu-id="0e5cf-101">Test-AzSignalRName</span><span class="sxs-lookup"><span data-stu-id="0e5cf-101">Test-AzSignalRName</span></span>

## <span data-ttu-id="0e5cf-102">Sammanfattning</span><span class="sxs-lookup"><span data-stu-id="0e5cf-102">SYNOPSIS</span></span>
<span data-ttu-id="0e5cf-103">Kontrol lera tillgängligheten för ett namn.</span><span class="sxs-lookup"><span data-stu-id="0e5cf-103">Check the availability of a name.</span></span> <span data-ttu-id="0e5cf-104">Alias: test-AzSignal.</span><span class="sxs-lookup"><span data-stu-id="0e5cf-104">Alias: Test-AzSignal.</span></span>

## <span data-ttu-id="0e5cf-105">FRÅGESYNTAXEN</span><span class="sxs-lookup"><span data-stu-id="0e5cf-105">SYNTAX</span></span>

```
Test-AzSignalRName [-Name] <String> [-Location] <String> [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

## <span data-ttu-id="0e5cf-106">PROBLEMBESKRIVNING</span><span class="sxs-lookup"><span data-stu-id="0e5cf-106">DESCRIPTION</span></span>
<span data-ttu-id="0e5cf-107">Kontrol lera tillgängligheten för ett namn.</span><span class="sxs-lookup"><span data-stu-id="0e5cf-107">Check the availability of a name.</span></span> <span data-ttu-id="0e5cf-108">Alias: test-AzSignal.</span><span class="sxs-lookup"><span data-stu-id="0e5cf-108">Alias: Test-AzSignal.</span></span>

## <span data-ttu-id="0e5cf-109">BESKRIVS</span><span class="sxs-lookup"><span data-stu-id="0e5cf-109">EXAMPLES</span></span>

### <span data-ttu-id="0e5cf-110">Kontrol lera ett förnamn.</span><span class="sxs-lookup"><span data-stu-id="0e5cf-110">Check an existed name.</span></span>
```powershell
PS C:\> Test-AzSignalRName -Name existedsignalr -Location eastus
False
```

### <span data-ttu-id="0e5cf-111">Markera ett namn som inte finns.</span><span class="sxs-lookup"><span data-stu-id="0e5cf-111">Check an unexisted name.</span></span>
```
powershell
PS C:\> Test-AzSignalR unexistedsignalr eastus
True
```

## <span data-ttu-id="0e5cf-112">MALLPARAMETRAR</span><span class="sxs-lookup"><span data-stu-id="0e5cf-112">PARAMETERS</span></span>

### <span data-ttu-id="0e5cf-113">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="0e5cf-113">-DefaultProfile</span></span>
<span data-ttu-id="0e5cf-114">Autentiseringsuppgifter, konto, klient organisation och abonnemang som används för kommunikation med Azure.</span><span class="sxs-lookup"><span data-stu-id="0e5cf-114">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="0e5cf-115">-Plats</span><span class="sxs-lookup"><span data-stu-id="0e5cf-115">-Location</span></span>
<span data-ttu-id="0e5cf-116">Signal tjänstens plats.</span><span class="sxs-lookup"><span data-stu-id="0e5cf-116">The SignalR service location.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: True
Position: 1
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="0e5cf-117">-Namn</span><span class="sxs-lookup"><span data-stu-id="0e5cf-117">-Name</span></span>
<span data-ttu-id="0e5cf-118">Namn på signal tjänst.</span><span class="sxs-lookup"><span data-stu-id="0e5cf-118">The SignalR service name.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: True
Position: 0
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="0e5cf-119">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="0e5cf-119">CommonParameters</span></span>
<span data-ttu-id="0e5cf-120">Den här cmdleten har stöd för de gemensamma parametrarna:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-disvariable,-utbuffer,-PipelineVariable,-verbose,-WarningAction och-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="0e5cf-120">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="0e5cf-121">Mer information finns i [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="0e5cf-121">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="0e5cf-122">KOSTNADS</span><span class="sxs-lookup"><span data-stu-id="0e5cf-122">INPUTS</span></span>

### <span data-ttu-id="0e5cf-123">System. String</span><span class="sxs-lookup"><span data-stu-id="0e5cf-123">System.String</span></span>

## <span data-ttu-id="0e5cf-124">VÄRDEN</span><span class="sxs-lookup"><span data-stu-id="0e5cf-124">OUTPUTS</span></span>

### <span data-ttu-id="0e5cf-125">System. Boolean</span><span class="sxs-lookup"><span data-stu-id="0e5cf-125">System.Boolean</span></span>

## <span data-ttu-id="0e5cf-126">ANMÄRKNINGAR</span><span class="sxs-lookup"><span data-stu-id="0e5cf-126">NOTES</span></span>

## <span data-ttu-id="0e5cf-127">RELATERADE LÄNKAR</span><span class="sxs-lookup"><span data-stu-id="0e5cf-127">RELATED LINKS</span></span>
