---
external help file: Microsoft.Azure.Commands.Compute.dll-Help.xml
Module Name: AzureRM.Compute
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.compute/get-azurermvmruncommanddocument
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Compute/Commands.Compute/help/Get-AzureRmVMRunCommandDocument.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Compute/Commands.Compute/help/Get-AzureRmVMRunCommandDocument.md
ms.openlocfilehash: 070fe50f74db08caab375a97d4d8ff6be3e970ae
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: sv-SE
ms.lasthandoff: 08/20/2020
ms.locfileid: "93576317"
---
# <span data-ttu-id="7e270-101">Get-AzureRmVMRunCommandDocument</span><span class="sxs-lookup"><span data-stu-id="7e270-101">Get-AzureRmVMRunCommandDocument</span></span>

## <span data-ttu-id="7e270-102">Sammanfattning</span><span class="sxs-lookup"><span data-stu-id="7e270-102">SYNOPSIS</span></span>
<span data-ttu-id="7e270-103">Kommandot Hämta kommando.</span><span class="sxs-lookup"><span data-stu-id="7e270-103">Get run command document.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="7e270-104">FRÅGESYNTAXEN</span><span class="sxs-lookup"><span data-stu-id="7e270-104">SYNTAX</span></span>

```
Get-AzureRmVMRunCommandDocument [-Location] <String> [[-CommandId] <String>]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="7e270-105">PROBLEMBESKRIVNING</span><span class="sxs-lookup"><span data-stu-id="7e270-105">DESCRIPTION</span></span>
<span data-ttu-id="7e270-106">Kommandot Hämta kommando.</span><span class="sxs-lookup"><span data-stu-id="7e270-106">Get run command document.</span></span>

## <span data-ttu-id="7e270-107">BESKRIVS</span><span class="sxs-lookup"><span data-stu-id="7e270-107">EXAMPLES</span></span>

### <span data-ttu-id="7e270-108">Exempel 1</span><span class="sxs-lookup"><span data-stu-id="7e270-108">Example 1</span></span>
```
PS C:\> Get-AzureRmVMRunCommandDocument -Location 'westus' -CommandId 'RunPowerShellScript'
```

<span data-ttu-id="7e270-109">Hämtar ett specifikt kommando dokument för "RunPowerShellScript" i "västkusten".</span><span class="sxs-lookup"><span data-stu-id="7e270-109">Gets a specific run command document for 'RunPowerShellScript' in 'westus'.</span></span>
<span data-ttu-id="7e270-110">Get-AzureRmVMRunCommandDocument plats $loc</span><span class="sxs-lookup"><span data-stu-id="7e270-110">Get-AzureRmVMRunCommandDocument -Location $loc</span></span>

### <span data-ttu-id="7e270-111">Exempel 2</span><span class="sxs-lookup"><span data-stu-id="7e270-111">Example 2</span></span>
```
PS C:\> Get-AzureRmVMRunCommandDocument -Location 'westus'
```

<span data-ttu-id="7e270-112">Visar alla tillgängliga kör-kommandon i "västkusten".</span><span class="sxs-lookup"><span data-stu-id="7e270-112">Lists all available run commands in 'westus'.</span></span>

## <span data-ttu-id="7e270-113">MALLPARAMETRAR</span><span class="sxs-lookup"><span data-stu-id="7e270-113">PARAMETERS</span></span>

### <span data-ttu-id="7e270-114">-CommandId</span><span class="sxs-lookup"><span data-stu-id="7e270-114">-CommandId</span></span>
<span data-ttu-id="7e270-115">Kommando-ID.</span><span class="sxs-lookup"><span data-stu-id="7e270-115">The command id.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: False
Position: 2
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="7e270-116">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="7e270-116">-DefaultProfile</span></span>
<span data-ttu-id="7e270-117">Autentiseringsuppgifter, konto, klient organisation och abonnemang som används för kommunikation med Azure.</span><span class="sxs-lookup"><span data-stu-id="7e270-117">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="7e270-118">-Plats</span><span class="sxs-lookup"><span data-stu-id="7e270-118">-Location</span></span>
<span data-ttu-id="7e270-119">Den plats där kommandona körs.</span><span class="sxs-lookup"><span data-stu-id="7e270-119">The location upon which run commands is queried.</span></span>

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

### <span data-ttu-id="7e270-120">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="7e270-120">CommonParameters</span></span>
<span data-ttu-id="7e270-121">Den här cmdleten har stöd för de gemensamma parametrarna:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-disvariable,-utbuffer,-PipelineVariable,-verbose,-WarningAction och-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="7e270-121">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="7e270-122">Mer information finns i about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="7e270-122">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="7e270-123">KOSTNADS</span><span class="sxs-lookup"><span data-stu-id="7e270-123">INPUTS</span></span>

### <span data-ttu-id="7e270-124">System. String</span><span class="sxs-lookup"><span data-stu-id="7e270-124">System.String</span></span>

## <span data-ttu-id="7e270-125">VÄRDEN</span><span class="sxs-lookup"><span data-stu-id="7e270-125">OUTPUTS</span></span>

### <span data-ttu-id="7e270-126">Microsoft. Azure. commands. Compute. Automation. Models. PSRunCommandDocument</span><span class="sxs-lookup"><span data-stu-id="7e270-126">Microsoft.Azure.Commands.Compute.Automation.Models.PSRunCommandDocument</span></span>

## <span data-ttu-id="7e270-127">ANMÄRKNINGAR</span><span class="sxs-lookup"><span data-stu-id="7e270-127">NOTES</span></span>

## <span data-ttu-id="7e270-128">RELATERADE LÄNKAR</span><span class="sxs-lookup"><span data-stu-id="7e270-128">RELATED LINKS</span></span>
