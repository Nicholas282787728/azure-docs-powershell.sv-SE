---
external help file: Microsoft.Azure.PowerShell.Cmdlets.LogicApp.dll-Help.xml
Module Name: Az.LogicApp
ms.assetid: B7FED447-C398-47D7-AF1B-A3E4FDAD0B41
online version: https://docs.microsoft.com/en-us/powershell/module/az.logicapp/get-azlogicappupgradeddefinition
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/LogicApp/LogicApp/help/Get-AzLogicAppUpgradedDefinition.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/LogicApp/LogicApp/help/Get-AzLogicAppUpgradedDefinition.md
ms.openlocfilehash: 2c0eb437aaa8a280b970e9c2a210b37b8fbce2d8
ms.sourcegitcommit: 1de2b6c3c99197958fa2101bc37680e7507f91ac
ms.translationtype: MT
ms.contentlocale: sv-SE
ms.lasthandoff: 10/13/2020
ms.locfileid: "94262209"
---
# <span data-ttu-id="97ed7-101">Get-AzLogicAppUpgradedDefinition</span><span class="sxs-lookup"><span data-stu-id="97ed7-101">Get-AzLogicAppUpgradedDefinition</span></span>

## <span data-ttu-id="97ed7-102">Sammanfattning</span><span class="sxs-lookup"><span data-stu-id="97ed7-102">SYNOPSIS</span></span>
<span data-ttu-id="97ed7-103">Hämtar den uppgraderade definitionen för en logik-app.</span><span class="sxs-lookup"><span data-stu-id="97ed7-103">Gets the upgraded definition for a logic app.</span></span>

## <span data-ttu-id="97ed7-104">FRÅGESYNTAXEN</span><span class="sxs-lookup"><span data-stu-id="97ed7-104">SYNTAX</span></span>

```
Get-AzLogicAppUpgradedDefinition -ResourceGroupName <String> -Name <String> -TargetSchemaVersion <String>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="97ed7-105">PROBLEMBESKRIVNING</span><span class="sxs-lookup"><span data-stu-id="97ed7-105">DESCRIPTION</span></span>
<span data-ttu-id="97ed7-106">Cmdleten **Get-AzLogicAppUpgradedDefinition** hämtar den uppgraderade definitionen för schema versionen och logik programmet från en resurs grupp.</span><span class="sxs-lookup"><span data-stu-id="97ed7-106">The **Get-AzLogicAppUpgradedDefinition** cmdlet gets the upgraded definition for the schema version and logic app from a resource group.</span></span>
<span data-ttu-id="97ed7-107">Denna cmdlet returnerar ett objekt som representerar definitionen av det uppgraderade logik programmet.</span><span class="sxs-lookup"><span data-stu-id="97ed7-107">This cmdlet returns an object that represents the definition of the upgraded logic app.</span></span>
<span data-ttu-id="97ed7-108">Ange resurs grupp namn, logik program namn och mål schema version.</span><span class="sxs-lookup"><span data-stu-id="97ed7-108">Specify the resource group name, logic app name, and target schema version.</span></span>
<span data-ttu-id="97ed7-109">Den här modulen stöder dynamiska parametrar.</span><span class="sxs-lookup"><span data-stu-id="97ed7-109">This module supports dynamic parameters.</span></span>
<span data-ttu-id="97ed7-110">Om du vill använda en dynamisk parameter skriver du den i kommandot.</span><span class="sxs-lookup"><span data-stu-id="97ed7-110">To use a dynamic parameter, type it in the command.</span></span>
<span data-ttu-id="97ed7-111">Om du vill söka efter namn på dynamiska parametrar skriver du ett bindestreck (-) efter cmdlet-namnet och trycker sedan på TABB-tangenten flera gånger för att växla mellan de tillgängliga parametrarna.</span><span class="sxs-lookup"><span data-stu-id="97ed7-111">To discover the names of dynamic parameters, type a hyphen (-) after the cmdlet name, and then press the Tab key repeatedly to cycle through the available parameters.</span></span>
<span data-ttu-id="97ed7-112">Om du utelämnar en obligatorisk mallparameter frågar cmdleten efter värdet.</span><span class="sxs-lookup"><span data-stu-id="97ed7-112">If you omit a required template parameter, the cmdlet prompts you for the value.</span></span>

## <span data-ttu-id="97ed7-113">BESKRIVS</span><span class="sxs-lookup"><span data-stu-id="97ed7-113">EXAMPLES</span></span>

### <span data-ttu-id="97ed7-114">Exempel 1: skaffa en väluppgraderad definition för logik</span><span class="sxs-lookup"><span data-stu-id="97ed7-114">Example 1: Get a logic app upgraded definition</span></span>
```
PS C:\>$UpgradedDefinition = Get-AzLogicAppUpgradedDefinition -ResourceGroupName "ResourceGroup11" -Name "LogicApp01" -TargetSchemaVersion "2016-06-01"
$UpgradedDefinition.ToString()
{

  "$schema": "http://schema.management.azure.com/providers/Microsoft.Logic/schemas/2016-06-01/workflowdefinition.json#",

  "contentVersion": "1.0.0.0",

  "parameters": {},

  "triggers": {

    "httpTrigger": {

      "recurrence": {

        "frequency": "Hour",

        "interval": 1

      },

      "type": "Http",

      "inputs": {

        "method": "GET",

        "uri": "http://www.bing.com"

      },

      "conditions": [

        {

          "expression": "@bool('true')" 

        }

      ] 

    },

    "manualTrigger": {

      "type": "Request",

      "kind": "Http"

    }

  },

  "actions": {

    "httpScope": {

      "actions": {

        "http": {

          "runAfter": {},

          "type": "Http",

          "inputs": {

            "method": "GET",

            "uri": "http://www.bing.com"

          }

        }

      },

      "runAfter": {},

      "else": {

        "actions": {}

      },

      "expression": "@bool('true')", 

      "type": "If"

    },

    "http1Scope": {

      "actions": {

        "http1": {

          "runAfter": {},

          "type": "Http",

          "inputs": {

            "method": "GET",

            "uri": "http://www.bing.com"

          }

        }

      },

      "runAfter": {},

      "else": {

        "actions": {}

      },

      "expression": "@bool('true')", 

      "type": "If"

    }

  },

  "outputs": {

    "output1": {

      "type": "String",

      "value": "true"

    }

  }

}
```

<span data-ttu-id="97ed7-115">Det första kommandot får definitionen för logik programmet som uppgraderats till den angivna mål schema versionen.</span><span class="sxs-lookup"><span data-stu-id="97ed7-115">The first command gets the definition for the logic app upgraded to the specified target schema version.</span></span>
<span data-ttu-id="97ed7-116">Kommandot lagrar definitionen i variabeln $UpgradedDefinition.</span><span class="sxs-lookup"><span data-stu-id="97ed7-116">The command stores the definition in the $UpgradedDefinition variable.</span></span>
<span data-ttu-id="97ed7-117">Det andra kommandot visar innehållet i $UpgradedDefinition som en sträng.</span><span class="sxs-lookup"><span data-stu-id="97ed7-117">The second command displays the contents of $UpgradedDefinition as a string.</span></span>

## <span data-ttu-id="97ed7-118">MALLPARAMETRAR</span><span class="sxs-lookup"><span data-stu-id="97ed7-118">PARAMETERS</span></span>

### <span data-ttu-id="97ed7-119">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="97ed7-119">-DefaultProfile</span></span>
<span data-ttu-id="97ed7-120">Autentiseringsuppgifter, konto, klient organisation och abonnemang som används för kommunikation med Azure</span><span class="sxs-lookup"><span data-stu-id="97ed7-120">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="97ed7-121">-Namn</span><span class="sxs-lookup"><span data-stu-id="97ed7-121">-Name</span></span>
<span data-ttu-id="97ed7-122">Anger namnet på en logik-app.</span><span class="sxs-lookup"><span data-stu-id="97ed7-122">Specifies the name of a logic app.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases: ResourceName

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="97ed7-123">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="97ed7-123">-ResourceGroupName</span></span>
<span data-ttu-id="97ed7-124">Anger namnet på en resurs grupp.</span><span class="sxs-lookup"><span data-stu-id="97ed7-124">Specifies the name of a resource group.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="97ed7-125">-TargetSchemaVersion</span><span class="sxs-lookup"><span data-stu-id="97ed7-125">-TargetSchemaVersion</span></span>
<span data-ttu-id="97ed7-126">Anger mål schema versionen för definitionen.</span><span class="sxs-lookup"><span data-stu-id="97ed7-126">Specifies the target schema version of the definition.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="97ed7-127">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="97ed7-127">CommonParameters</span></span>
<span data-ttu-id="97ed7-128">Den här cmdleten har stöd för de gemensamma parametrarna:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-disvariable,-utbuffer,-PipelineVariable,-verbose,-WarningAction och-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="97ed7-128">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="97ed7-129">Mer information finns i about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="97ed7-129">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="97ed7-130">KOSTNADS</span><span class="sxs-lookup"><span data-stu-id="97ed7-130">INPUTS</span></span>

### <span data-ttu-id="97ed7-131">System. String</span><span class="sxs-lookup"><span data-stu-id="97ed7-131">System.String</span></span>

## <span data-ttu-id="97ed7-132">VÄRDEN</span><span class="sxs-lookup"><span data-stu-id="97ed7-132">OUTPUTS</span></span>

### <span data-ttu-id="97ed7-133">System. Object</span><span class="sxs-lookup"><span data-stu-id="97ed7-133">System.Object</span></span>

## <span data-ttu-id="97ed7-134">ANMÄRKNINGAR</span><span class="sxs-lookup"><span data-stu-id="97ed7-134">NOTES</span></span>

## <span data-ttu-id="97ed7-135">RELATERADE LÄNKAR</span><span class="sxs-lookup"><span data-stu-id="97ed7-135">RELATED LINKS</span></span>

[<span data-ttu-id="97ed7-136">Get-AzLogicApp</span><span class="sxs-lookup"><span data-stu-id="97ed7-136">Get-AzLogicApp</span></span>](./Get-AzLogicApp.md)


