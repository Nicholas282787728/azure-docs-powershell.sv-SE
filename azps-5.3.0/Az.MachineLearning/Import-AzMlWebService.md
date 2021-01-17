---
external help file: Microsoft.Azure.PowerShell.Cmdlets.MachineLearning.dll-Help.xml
Module Name: Az.MachineLearning
online version: https://docs.microsoft.com/en-us/powershell/module/az.machinelearning/import-azmlwebservice
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/MachineLearning/MachineLearning/help/Import-AzMlWebService.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/MachineLearning/MachineLearning/help/Import-AzMlWebService.md
ms.openlocfilehash: 90416cd786e13bdd0232aebfcff2cd6963c1f872
ms.sourcegitcommit: 68451baa389791703e666d95469602c5652609ee
ms.translationtype: MT
ms.contentlocale: sv-SE
ms.lasthandoff: 01/05/2021
ms.locfileid: "98425632"
---
# <span data-ttu-id="b7092-101">Import-AzMlWebService</span><span class="sxs-lookup"><span data-stu-id="b7092-101">Import-AzMlWebService</span></span>

## <span data-ttu-id="b7092-102">Sammanfattning</span><span class="sxs-lookup"><span data-stu-id="b7092-102">SYNOPSIS</span></span>
<span data-ttu-id="b7092-103">Importerar ett JSON-objekt till en webb tjänst definition.</span><span class="sxs-lookup"><span data-stu-id="b7092-103">Imports a JSON object into a web service definition.</span></span>

## <span data-ttu-id="b7092-104">FRÅGESYNTAXEN</span><span class="sxs-lookup"><span data-stu-id="b7092-104">SYNTAX</span></span>

### <span data-ttu-id="b7092-105">ImportFromJSONFile</span><span class="sxs-lookup"><span data-stu-id="b7092-105">ImportFromJSONFile</span></span>
```
Import-AzMlWebService -InputFile <String> [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="b7092-106">ImportFromJSONString.</span><span class="sxs-lookup"><span data-stu-id="b7092-106">ImportFromJSONString.</span></span>
```
Import-AzMlWebService -JsonString <String> [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="b7092-107">PROBLEMBESKRIVNING</span><span class="sxs-lookup"><span data-stu-id="b7092-107">DESCRIPTION</span></span>
<span data-ttu-id="b7092-108">Import-AzMlWebService cmdlet importeras, anges antingen direkt eller i en refererad fil, och skapar ett webb tjänst definitions objekt som kan skickas till New-AzMlWebService cmdlet.</span><span class="sxs-lookup"><span data-stu-id="b7092-108">The Import-AzMlWebService cmdlet imports , specified either directly or in a referenced file, and creates a web service definition object that can be passed to the New-AzMlWebService cmdlet.</span></span>

## <span data-ttu-id="b7092-109">BESKRIVS</span><span class="sxs-lookup"><span data-stu-id="b7092-109">EXAMPLES</span></span>

### <span data-ttu-id="b7092-110">Exempel 1: importera från sträng</span><span class="sxs-lookup"><span data-stu-id="b7092-110">Example 1: Import from string</span></span>
```
Import-AzMlWebService -JsonString $jsonDefinition
```

### <span data-ttu-id="b7092-111">Exempel 2: importera från fil Sök väg</span><span class="sxs-lookup"><span data-stu-id="b7092-111">Example 2: Import from file path</span></span>
```
Import-AzMlWebService -InputFile "C:\mlservice.json"
```

## <span data-ttu-id="b7092-112">MALLPARAMETRAR</span><span class="sxs-lookup"><span data-stu-id="b7092-112">PARAMETERS</span></span>

### <span data-ttu-id="b7092-113">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="b7092-113">-DefaultProfile</span></span>
<span data-ttu-id="b7092-114">Autentiseringsuppgifter, konto, klient organisation och abonnemang som används för kommunikation med Azure</span><span class="sxs-lookup"><span data-stu-id="b7092-114">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="b7092-115">-InputFile</span><span class="sxs-lookup"><span data-stu-id="b7092-115">-InputFile</span></span>
<span data-ttu-id="b7092-116">Sökvägen till filen som innehåller webb tjänst definitionen som ska importeras.</span><span class="sxs-lookup"><span data-stu-id="b7092-116">The path to the file containing the web service definition to import.</span></span>

```yaml
Type: System.String
Parameter Sets: ImportFromJSONFile
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="b7092-117">-JsonString</span><span class="sxs-lookup"><span data-stu-id="b7092-117">-JsonString</span></span>
<span data-ttu-id="b7092-118">Den JSON-formaterade sträng som innehåller webb tjänst definitionen som ska importeras.</span><span class="sxs-lookup"><span data-stu-id="b7092-118">The JSON formatted string containing the web service definition to import.</span></span>

```yaml
Type: System.String
Parameter Sets: ImportFromJSONString.
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="b7092-119">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="b7092-119">CommonParameters</span></span>
<span data-ttu-id="b7092-120">Den här cmdleten har stöd för de gemensamma parametrarna:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-disvariable,-utbuffer,-PipelineVariable,-verbose,-WarningAction och-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="b7092-120">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="b7092-121">Mer information finns i about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="b7092-121">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="b7092-122">KOSTNADS</span><span class="sxs-lookup"><span data-stu-id="b7092-122">INPUTS</span></span>

### <span data-ttu-id="b7092-123">Ingen</span><span class="sxs-lookup"><span data-stu-id="b7092-123">None</span></span>

## <span data-ttu-id="b7092-124">VÄRDEN</span><span class="sxs-lookup"><span data-stu-id="b7092-124">OUTPUTS</span></span>

### <span data-ttu-id="b7092-125">Microsoft. Azure. Management. MachineLearning. WebServices. Models. WebService</span><span class="sxs-lookup"><span data-stu-id="b7092-125">Microsoft.Azure.Management.MachineLearning.WebServices.Models.WebService</span></span>

## <span data-ttu-id="b7092-126">ANMÄRKNINGAR</span><span class="sxs-lookup"><span data-stu-id="b7092-126">NOTES</span></span>
<span data-ttu-id="b7092-127">Nyckelord: Azure, azurerm, arm, resurs, hantering, chef, maskin, maskin inlärning, azureml</span><span class="sxs-lookup"><span data-stu-id="b7092-127">Keywords: azure, azurerm, arm, resource, management, manager, machine, machine learning, azureml</span></span>

## <span data-ttu-id="b7092-128">RELATERADE LÄNKAR</span><span class="sxs-lookup"><span data-stu-id="b7092-128">RELATED LINKS</span></span>
