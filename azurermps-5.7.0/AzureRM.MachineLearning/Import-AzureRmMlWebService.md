---
external help file: Microsoft.Azure.Commands.MachineLearning.dll-Help.xml
Module Name: AzureRM.MachineLearning
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.machinelearning/import-azurermmlwebservice
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/MachineLearning/Commands.MachineLearning/help/Import-AzureRmMlWebService.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/MachineLearning/Commands.MachineLearning/help/Import-AzureRmMlWebService.md
ms.openlocfilehash: cc6c596b028ca7a4b89083ff06d37b3df9c3ed7a
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: sv-SE
ms.lasthandoff: 08/20/2020
ms.locfileid: "93578188"
---
# <span data-ttu-id="7c7e3-101">Import-AzureRmMlWebService</span><span class="sxs-lookup"><span data-stu-id="7c7e3-101">Import-AzureRmMlWebService</span></span>

## <span data-ttu-id="7c7e3-102">Sammanfattning</span><span class="sxs-lookup"><span data-stu-id="7c7e3-102">SYNOPSIS</span></span>
<span data-ttu-id="7c7e3-103">Importerar ett JSON-objekt till en webb tjänst definition.</span><span class="sxs-lookup"><span data-stu-id="7c7e3-103">Imports a JSON object into a web service definition.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="7c7e3-104">FRÅGESYNTAXEN</span><span class="sxs-lookup"><span data-stu-id="7c7e3-104">SYNTAX</span></span>

### <span data-ttu-id="7c7e3-105">ImportFromJSONFile</span><span class="sxs-lookup"><span data-stu-id="7c7e3-105">ImportFromJSONFile</span></span>
```
Import-AzureRmMlWebService -InputFile <String> [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="7c7e3-106">ImportFromJSONString.</span><span class="sxs-lookup"><span data-stu-id="7c7e3-106">ImportFromJSONString.</span></span>
```
Import-AzureRmMlWebService -JsonString <String> [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="7c7e3-107">PROBLEMBESKRIVNING</span><span class="sxs-lookup"><span data-stu-id="7c7e3-107">DESCRIPTION</span></span>
<span data-ttu-id="7c7e3-108">Import-AzureRmMlWebService cmdlet importeras, anges antingen direkt eller i en refererad fil, och skapar ett webb tjänst definitions objekt som kan skickas till New-AzureRmMlWebService cmdlet.</span><span class="sxs-lookup"><span data-stu-id="7c7e3-108">The Import-AzureRmMlWebService cmdlet imports , specified either directly or in a referenced file, and creates a web service definition object that can be passed to the New-AzureRmMlWebService cmdlet.</span></span>

## <span data-ttu-id="7c7e3-109">BESKRIVS</span><span class="sxs-lookup"><span data-stu-id="7c7e3-109">EXAMPLES</span></span>

### <span data-ttu-id="7c7e3-110">--------------------------Exempel 1: importera från sträng--------------------------</span><span class="sxs-lookup"><span data-stu-id="7c7e3-110">--------------------------  Example 1: Import from string  --------------------------</span></span>
```
Import-AzureRmMlWebService -JsonString $jsonDefinition
```

### <span data-ttu-id="7c7e3-111">--------------------------Exempel 2: importera från sökväg--------------------------</span><span class="sxs-lookup"><span data-stu-id="7c7e3-111">--------------------------  Example 2: Import from file path  --------------------------</span></span>
```
Import-AzureRmMlWebService -InputFile "C:\mlservice.json"
```

## <span data-ttu-id="7c7e3-112">MALLPARAMETRAR</span><span class="sxs-lookup"><span data-stu-id="7c7e3-112">PARAMETERS</span></span>

### <span data-ttu-id="7c7e3-113">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="7c7e3-113">-DefaultProfile</span></span>
<span data-ttu-id="7c7e3-114">Autentiseringsuppgifter, konto, klient organisation och abonnemang som används för kommunikation med Azure</span><span class="sxs-lookup"><span data-stu-id="7c7e3-114">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="7c7e3-115">-InputFile</span><span class="sxs-lookup"><span data-stu-id="7c7e3-115">-InputFile</span></span>
<span data-ttu-id="7c7e3-116">Sökvägen till filen som innehåller webb tjänst definitionen som ska importeras.</span><span class="sxs-lookup"><span data-stu-id="7c7e3-116">The path to the file containing the web service definition to import.</span></span>

```yaml
Type: String
Parameter Sets: ImportFromJSONFile
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="7c7e3-117">-JsonString</span><span class="sxs-lookup"><span data-stu-id="7c7e3-117">-JsonString</span></span>
<span data-ttu-id="7c7e3-118">Den JSON-formaterade sträng som innehåller webb tjänst definitionen som ska importeras.</span><span class="sxs-lookup"><span data-stu-id="7c7e3-118">The JSON formatted string containing the web service definition to import.</span></span>

```yaml
Type: String
Parameter Sets: ImportFromJSONString.
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="7c7e3-119">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="7c7e3-119">CommonParameters</span></span>
<span data-ttu-id="7c7e3-120">Den här cmdleten har stöd för de gemensamma parametrarna:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-disvariable,-utbuffer,-PipelineVariable,-verbose,-WarningAction och-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="7c7e3-120">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="7c7e3-121">Mer information finns i about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="7c7e3-121">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="7c7e3-122">KOSTNADS</span><span class="sxs-lookup"><span data-stu-id="7c7e3-122">INPUTS</span></span>

### <span data-ttu-id="7c7e3-123">Ingen</span><span class="sxs-lookup"><span data-stu-id="7c7e3-123">None</span></span>
<span data-ttu-id="7c7e3-124">Denna cmdlet accepterar inte indata.</span><span class="sxs-lookup"><span data-stu-id="7c7e3-124">This cmdlet does not accept any input.</span></span>

## <span data-ttu-id="7c7e3-125">VÄRDEN</span><span class="sxs-lookup"><span data-stu-id="7c7e3-125">OUTPUTS</span></span>

### <span data-ttu-id="7c7e3-126">Microsoft. Azure. Management. MachineLearning. WebServices. Models. WebService</span><span class="sxs-lookup"><span data-stu-id="7c7e3-126">Microsoft.Azure.Management.MachineLearning.WebServices.Models.WebService</span></span>

## <span data-ttu-id="7c7e3-127">ANMÄRKNINGAR</span><span class="sxs-lookup"><span data-stu-id="7c7e3-127">NOTES</span></span>
<span data-ttu-id="7c7e3-128">Nyckelord: Azure, azurerm, arm, resurs, hantering, chef, maskin, maskin inlärning, azureml</span><span class="sxs-lookup"><span data-stu-id="7c7e3-128">Keywords: azure, azurerm, arm, resource, management, manager, machine, machine learning, azureml</span></span>

## <span data-ttu-id="7c7e3-129">RELATERADE LÄNKAR</span><span class="sxs-lookup"><span data-stu-id="7c7e3-129">RELATED LINKS</span></span>

