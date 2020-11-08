---
external help file: Microsoft.Azure.PowerShell.Cmdlets.SignalR.dll-Help.xml
Module Name: Az.SignalR
online version: https://docs.microsoft.com/en-us/powershell/module/az.signalr/test-azsignalrname
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/SignalR/SignalR/help/Test-AzSignalRName.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/SignalR/SignalR/help/Test-AzSignalRName.md
ms.openlocfilehash: 21fbee422b898b5e5cf448f4a8f1913777268964
ms.sourcegitcommit: 4d2c178cd6df9151877b08d54c1f4a228dbec9d1
ms.translationtype: MT
ms.contentlocale: sv-SE
ms.lasthandoff: 01/29/2020
ms.locfileid: "93919138"
---
# <span data-ttu-id="d97f1-101">Test-AzSignalRName</span><span class="sxs-lookup"><span data-stu-id="d97f1-101">Test-AzSignalRName</span></span>

## <span data-ttu-id="d97f1-102">Sammanfattning</span><span class="sxs-lookup"><span data-stu-id="d97f1-102">SYNOPSIS</span></span>
<span data-ttu-id="d97f1-103">Kontrol lera tillgängligheten för ett namn.</span><span class="sxs-lookup"><span data-stu-id="d97f1-103">Check the availability of a name.</span></span> <span data-ttu-id="d97f1-104">Alias: test-AzSignal.</span><span class="sxs-lookup"><span data-stu-id="d97f1-104">Alias: Test-AzSignal.</span></span>

## <span data-ttu-id="d97f1-105">FRÅGESYNTAXEN</span><span class="sxs-lookup"><span data-stu-id="d97f1-105">SYNTAX</span></span>

```
Test-AzSignalRName [-Name] <String> [-Location] <String> [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

## <span data-ttu-id="d97f1-106">PROBLEMBESKRIVNING</span><span class="sxs-lookup"><span data-stu-id="d97f1-106">DESCRIPTION</span></span>
<span data-ttu-id="d97f1-107">Kontrol lera tillgängligheten för ett namn.</span><span class="sxs-lookup"><span data-stu-id="d97f1-107">Check the availability of a name.</span></span> <span data-ttu-id="d97f1-108">Alias: test-AzSignal.</span><span class="sxs-lookup"><span data-stu-id="d97f1-108">Alias: Test-AzSignal.</span></span>

## <span data-ttu-id="d97f1-109">BESKRIVS</span><span class="sxs-lookup"><span data-stu-id="d97f1-109">EXAMPLES</span></span>

### <span data-ttu-id="d97f1-110">Kontrol lera ett förnamn.</span><span class="sxs-lookup"><span data-stu-id="d97f1-110">Check an existed name.</span></span>
```powershell
PS C:\> Test-AzSignalRName -Name existedsignalr -Location eastus
False
```

### <span data-ttu-id="d97f1-111">Markera ett namn som inte finns.</span><span class="sxs-lookup"><span data-stu-id="d97f1-111">Check an unexisted name.</span></span>
```
powershell
PS C:\> Test-AzSignalR unexistedsignalr eastus
True
```

## <span data-ttu-id="d97f1-112">MALLPARAMETRAR</span><span class="sxs-lookup"><span data-stu-id="d97f1-112">PARAMETERS</span></span>

### <span data-ttu-id="d97f1-113">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="d97f1-113">-DefaultProfile</span></span>
<span data-ttu-id="d97f1-114">Autentiseringsuppgifter, konto, klient organisation och abonnemang som används för kommunikation med Azure.</span><span class="sxs-lookup"><span data-stu-id="d97f1-114">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="d97f1-115">-Plats</span><span class="sxs-lookup"><span data-stu-id="d97f1-115">-Location</span></span>
<span data-ttu-id="d97f1-116">Signal tjänstens plats.</span><span class="sxs-lookup"><span data-stu-id="d97f1-116">The SignalR service location.</span></span>

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

### <span data-ttu-id="d97f1-117">-Namn</span><span class="sxs-lookup"><span data-stu-id="d97f1-117">-Name</span></span>
<span data-ttu-id="d97f1-118">Namn på signal tjänst.</span><span class="sxs-lookup"><span data-stu-id="d97f1-118">The SignalR service name.</span></span>

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

### <span data-ttu-id="d97f1-119">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="d97f1-119">CommonParameters</span></span>
<span data-ttu-id="d97f1-120">Den här cmdleten har stöd för de gemensamma parametrarna:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-disvariable,-utbuffer,-PipelineVariable,-verbose,-WarningAction och-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="d97f1-120">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="d97f1-121">Mer information finns i [about_CommonParameters](https://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="d97f1-121">For more information, see [about_CommonParameters](https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="d97f1-122">KOSTNADS</span><span class="sxs-lookup"><span data-stu-id="d97f1-122">INPUTS</span></span>

### <span data-ttu-id="d97f1-123">System. String</span><span class="sxs-lookup"><span data-stu-id="d97f1-123">System.String</span></span>

## <span data-ttu-id="d97f1-124">VÄRDEN</span><span class="sxs-lookup"><span data-stu-id="d97f1-124">OUTPUTS</span></span>

### <span data-ttu-id="d97f1-125">System. Boolean</span><span class="sxs-lookup"><span data-stu-id="d97f1-125">System.Boolean</span></span>

## <span data-ttu-id="d97f1-126">ANMÄRKNINGAR</span><span class="sxs-lookup"><span data-stu-id="d97f1-126">NOTES</span></span>

## <span data-ttu-id="d97f1-127">RELATERADE LÄNKAR</span><span class="sxs-lookup"><span data-stu-id="d97f1-127">RELATED LINKS</span></span>