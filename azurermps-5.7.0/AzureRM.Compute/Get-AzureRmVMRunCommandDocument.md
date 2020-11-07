---
external help file: Microsoft.Azure.Commands.Compute.dll-Help.xml
Module Name: AzureRM.Compute
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.compute/get-azurermvmruncommanddocument
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Compute/Commands.Compute/help/Get-AzureRmVMRunCommandDocument.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Compute/Commands.Compute/help/Get-AzureRmVMRunCommandDocument.md
ms.openlocfilehash: df53acc047ff0c17b3482f214c357f66ce638efb
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: sv-SE
ms.lasthandoff: 08/20/2020
ms.locfileid: "93757707"
---
# <span data-ttu-id="1177c-101">Get-AzureRmVMRunCommandDocument</span><span class="sxs-lookup"><span data-stu-id="1177c-101">Get-AzureRmVMRunCommandDocument</span></span>

## <span data-ttu-id="1177c-102">Sammanfattning</span><span class="sxs-lookup"><span data-stu-id="1177c-102">SYNOPSIS</span></span>
<span data-ttu-id="1177c-103">Kommandot Hämta kommando.</span><span class="sxs-lookup"><span data-stu-id="1177c-103">Get run command document.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="1177c-104">FRÅGESYNTAXEN</span><span class="sxs-lookup"><span data-stu-id="1177c-104">SYNTAX</span></span>

```
Get-AzureRmVMRunCommandDocument [-Location] <String> [[-CommandId] <String>]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="1177c-105">PROBLEMBESKRIVNING</span><span class="sxs-lookup"><span data-stu-id="1177c-105">DESCRIPTION</span></span>
<span data-ttu-id="1177c-106">Kommandot Hämta kommando.</span><span class="sxs-lookup"><span data-stu-id="1177c-106">Get run command document.</span></span>

## <span data-ttu-id="1177c-107">BESKRIVS</span><span class="sxs-lookup"><span data-stu-id="1177c-107">EXAMPLES</span></span>

### <span data-ttu-id="1177c-108">Exempel 1</span><span class="sxs-lookup"><span data-stu-id="1177c-108">Example 1</span></span>
```
PS C:\> Get-AzureRmVMRunCommandDocument -Location 'westus' -CommandId 'RunPowerShellScript'
```

<span data-ttu-id="1177c-109">Hämtar ett specifikt kommando dokument för "RunPowerShellScript" i "västkusten".</span><span class="sxs-lookup"><span data-stu-id="1177c-109">Gets a specific run command document for 'RunPowerShellScript' in 'westus'.</span></span>


<span data-ttu-id="1177c-110">Get-AzureRmVMRunCommandDocument plats $loc</span><span class="sxs-lookup"><span data-stu-id="1177c-110">Get-AzureRmVMRunCommandDocument -Location $loc</span></span>

### <span data-ttu-id="1177c-111">Exempel 2</span><span class="sxs-lookup"><span data-stu-id="1177c-111">Example 2</span></span>
```
PS C:\> Get-AzureRmVMRunCommandDocument -Location 'westus'
```

<span data-ttu-id="1177c-112">Visar alla tillgängliga kör-kommandon i "västkusten".</span><span class="sxs-lookup"><span data-stu-id="1177c-112">Lists all available run commands in 'westus'.</span></span>

## <span data-ttu-id="1177c-113">MALLPARAMETRAR</span><span class="sxs-lookup"><span data-stu-id="1177c-113">PARAMETERS</span></span>

### <span data-ttu-id="1177c-114">-CommandId</span><span class="sxs-lookup"><span data-stu-id="1177c-114">-CommandId</span></span>
<span data-ttu-id="1177c-115">Kommando-ID.</span><span class="sxs-lookup"><span data-stu-id="1177c-115">The command id.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases:

Required: False
Position: 2
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="1177c-116">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="1177c-116">-DefaultProfile</span></span>
<span data-ttu-id="1177c-117">Autentiseringsuppgifter, konto, klient organisation och abonnemang som används för kommunikation med Azure.</span><span class="sxs-lookup"><span data-stu-id="1177c-117">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

```yaml
Type: IAzureContextContainer
Parameter Sets: (All)
Aliases: AzureRmContext, AzureCredential

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="1177c-118">-Plats</span><span class="sxs-lookup"><span data-stu-id="1177c-118">-Location</span></span>
<span data-ttu-id="1177c-119">Den plats där kommandona körs.</span><span class="sxs-lookup"><span data-stu-id="1177c-119">The location upon which run commands is queried.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases:

Required: True
Position: 1
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="1177c-120">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="1177c-120">CommonParameters</span></span>
<span data-ttu-id="1177c-121">Den här cmdleten har stöd för de gemensamma parametrarna:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-disvariable,-utbuffer,-PipelineVariable,-verbose,-WarningAction och-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="1177c-121">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="1177c-122">Mer information finns i about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="1177c-122">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="1177c-123">KOSTNADS</span><span class="sxs-lookup"><span data-stu-id="1177c-123">INPUTS</span></span>

### <span data-ttu-id="1177c-124">System. String</span><span class="sxs-lookup"><span data-stu-id="1177c-124">System.String</span></span>

## <span data-ttu-id="1177c-125">VÄRDEN</span><span class="sxs-lookup"><span data-stu-id="1177c-125">OUTPUTS</span></span>

### <span data-ttu-id="1177c-126">Microsoft. Azure. commands. Compute. Automation. Models. PSRunCommandDocument</span><span class="sxs-lookup"><span data-stu-id="1177c-126">Microsoft.Azure.Commands.Compute.Automation.Models.PSRunCommandDocument</span></span>

## <span data-ttu-id="1177c-127">ANMÄRKNINGAR</span><span class="sxs-lookup"><span data-stu-id="1177c-127">NOTES</span></span>

## <span data-ttu-id="1177c-128">RELATERADE LÄNKAR</span><span class="sxs-lookup"><span data-stu-id="1177c-128">RELATED LINKS</span></span>