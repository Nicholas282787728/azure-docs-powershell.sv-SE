---
external help file: Microsoft.Azure.PowerShell.Cmdlets.SignalR.dll-Help.xml
Module Name: Az.SignalR
online version: https://docs.microsoft.com/en-us/powershell/module/az.signalr/test-azsignalrname
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/SignalR/SignalR/help/Test-AzSignalRName.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/SignalR/SignalR/help/Test-AzSignalRName.md
ms.openlocfilehash: b00a408df2fe1705309152a02484d3b18ea41e9e
ms.sourcegitcommit: 04221336bc9eed46c05ed1e828a6811534d4b4ab
ms.translationtype: MT
ms.contentlocale: sv-SE
ms.lasthandoff: 12/08/2020
ms.locfileid: "98393312"
---
# <span data-ttu-id="b3495-101">Test-AzSignalRName</span><span class="sxs-lookup"><span data-stu-id="b3495-101">Test-AzSignalRName</span></span>

## <span data-ttu-id="b3495-102">Sammanfattning</span><span class="sxs-lookup"><span data-stu-id="b3495-102">SYNOPSIS</span></span>
<span data-ttu-id="b3495-103">Kontrol lera tillgängligheten för ett namn.</span><span class="sxs-lookup"><span data-stu-id="b3495-103">Check the availability of a name.</span></span> <span data-ttu-id="b3495-104">Alias: test-AzSignal.</span><span class="sxs-lookup"><span data-stu-id="b3495-104">Alias: Test-AzSignal.</span></span>

## <span data-ttu-id="b3495-105">FRÅGESYNTAXEN</span><span class="sxs-lookup"><span data-stu-id="b3495-105">SYNTAX</span></span>

```
Test-AzSignalRName [-Name] <String> [-Location] <String> [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

## <span data-ttu-id="b3495-106">PROBLEMBESKRIVNING</span><span class="sxs-lookup"><span data-stu-id="b3495-106">DESCRIPTION</span></span>
<span data-ttu-id="b3495-107">Kontrol lera tillgängligheten för ett namn.</span><span class="sxs-lookup"><span data-stu-id="b3495-107">Check the availability of a name.</span></span> <span data-ttu-id="b3495-108">Alias: test-AzSignal.</span><span class="sxs-lookup"><span data-stu-id="b3495-108">Alias: Test-AzSignal.</span></span>

## <span data-ttu-id="b3495-109">BESKRIVS</span><span class="sxs-lookup"><span data-stu-id="b3495-109">EXAMPLES</span></span>

### <span data-ttu-id="b3495-110">Kontrol lera ett förnamn.</span><span class="sxs-lookup"><span data-stu-id="b3495-110">Check an existed name.</span></span>
```powershell
PS C:\> Test-AzSignalRName -Name existedsignalr -Location eastus
False
```

### <span data-ttu-id="b3495-111">Markera ett namn som inte finns.</span><span class="sxs-lookup"><span data-stu-id="b3495-111">Check an unexisted name.</span></span>
```
powershell
PS C:\> Test-AzSignalR unexistedsignalr eastus
True
```

## <span data-ttu-id="b3495-112">MALLPARAMETRAR</span><span class="sxs-lookup"><span data-stu-id="b3495-112">PARAMETERS</span></span>

### <span data-ttu-id="b3495-113">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="b3495-113">-DefaultProfile</span></span>
<span data-ttu-id="b3495-114">Autentiseringsuppgifter, konto, klient organisation och abonnemang som används för kommunikation med Azure.</span><span class="sxs-lookup"><span data-stu-id="b3495-114">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="b3495-115">-Plats</span><span class="sxs-lookup"><span data-stu-id="b3495-115">-Location</span></span>
<span data-ttu-id="b3495-116">Signal tjänstens plats.</span><span class="sxs-lookup"><span data-stu-id="b3495-116">The SignalR service location.</span></span>

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

### <span data-ttu-id="b3495-117">-Namn</span><span class="sxs-lookup"><span data-stu-id="b3495-117">-Name</span></span>
<span data-ttu-id="b3495-118">Namn på signal tjänst.</span><span class="sxs-lookup"><span data-stu-id="b3495-118">The SignalR service name.</span></span>

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

### <span data-ttu-id="b3495-119">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="b3495-119">CommonParameters</span></span>
<span data-ttu-id="b3495-120">Den här cmdleten har stöd för de gemensamma parametrarna:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-disvariable,-utbuffer,-PipelineVariable,-verbose,-WarningAction och-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="b3495-120">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="b3495-121">Mer information finns i [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="b3495-121">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="b3495-122">KOSTNADS</span><span class="sxs-lookup"><span data-stu-id="b3495-122">INPUTS</span></span>

### <span data-ttu-id="b3495-123">System. String</span><span class="sxs-lookup"><span data-stu-id="b3495-123">System.String</span></span>

## <span data-ttu-id="b3495-124">VÄRDEN</span><span class="sxs-lookup"><span data-stu-id="b3495-124">OUTPUTS</span></span>

### <span data-ttu-id="b3495-125">System. Boolean</span><span class="sxs-lookup"><span data-stu-id="b3495-125">System.Boolean</span></span>

## <span data-ttu-id="b3495-126">ANMÄRKNINGAR</span><span class="sxs-lookup"><span data-stu-id="b3495-126">NOTES</span></span>

## <span data-ttu-id="b3495-127">RELATERADE LÄNKAR</span><span class="sxs-lookup"><span data-stu-id="b3495-127">RELATED LINKS</span></span>
