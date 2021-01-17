---
external help file: Microsoft.Azure.PowerShell.Cmdlets.ResourceManager.dll-Help.xml
Module Name: Az.Resources
online version: https://docs.microsoft.com/en-us/powershell/module/az.resources/get-azdeploymentscript
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Resources/Resources/help/Get-AzDeploymentScript.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Resources/Resources/help/Get-AzDeploymentScript.md
ms.openlocfilehash: b5c3ca86129e622a90a84d099961a8f8dd433eef
ms.sourcegitcommit: 04221336bc9eed46c05ed1e828a6811534d4b4ab
ms.translationtype: MT
ms.contentlocale: sv-SE
ms.lasthandoff: 12/08/2020
ms.locfileid: "98389034"
---
# <span data-ttu-id="798c6-101">Get-AzDeploymentScript</span><span class="sxs-lookup"><span data-stu-id="798c6-101">Get-AzDeploymentScript</span></span>

## <span data-ttu-id="798c6-102">Sammanfattning</span><span class="sxs-lookup"><span data-stu-id="798c6-102">SYNOPSIS</span></span>
<span data-ttu-id="798c6-103">Hämtar eller visar distributions skript.</span><span class="sxs-lookup"><span data-stu-id="798c6-103">Gets or lists deployment scripts.</span></span>

## <span data-ttu-id="798c6-104">FRÅGESYNTAXEN</span><span class="sxs-lookup"><span data-stu-id="798c6-104">SYNTAX</span></span>

### <span data-ttu-id="798c6-105">ListDeploymentScript (standard)</span><span class="sxs-lookup"><span data-stu-id="798c6-105">ListDeploymentScript (Default)</span></span>
```
Get-AzDeploymentScript [[-ResourceGroupName] <String>] [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

### <span data-ttu-id="798c6-106">GetDeploymentScriptByName</span><span class="sxs-lookup"><span data-stu-id="798c6-106">GetDeploymentScriptByName</span></span>
```
Get-AzDeploymentScript [-ResourceGroupName] <String> [-Name] <String>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="798c6-107">GetDeploymentScriptByResourceId</span><span class="sxs-lookup"><span data-stu-id="798c6-107">GetDeploymentScriptByResourceId</span></span>
```
Get-AzDeploymentScript [-Id] <String> [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="798c6-108">PROBLEMBESKRIVNING</span><span class="sxs-lookup"><span data-stu-id="798c6-108">DESCRIPTION</span></span>
<span data-ttu-id="798c6-109">Cmdleten **Get-AzDeploymentScript** hämtar ett enskilt distributions skript eller en lista med distributions skript.</span><span class="sxs-lookup"><span data-stu-id="798c6-109">The **Get-AzDeploymentScript** cmdlet gets a single deployment script or a list of deployment scripts.</span></span>

## <span data-ttu-id="798c6-110">BESKRIVS</span><span class="sxs-lookup"><span data-stu-id="798c6-110">EXAMPLES</span></span>

### <span data-ttu-id="798c6-111">Exempel 1</span><span class="sxs-lookup"><span data-stu-id="798c6-111">Example 1</span></span>
```powershell
PS C:\> Get-AzDeploymentScript
```

<span data-ttu-id="798c6-112">Visar en lista över distributions skript i prenumerationen i den aktuella användarens kontext.</span><span class="sxs-lookup"><span data-stu-id="798c6-112">Lists deployment scripts in the subscription in current user's context.</span></span>

### <span data-ttu-id="798c6-113">Exempel 2</span><span class="sxs-lookup"><span data-stu-id="798c6-113">Example 2</span></span>
```powershell
PS C:\> Get-AzDeploymentScript -ResourceGroupName DS-TestRg
```

<span data-ttu-id="798c6-114">Visar distributions skript i resurs gruppen DS-TestRg.</span><span class="sxs-lookup"><span data-stu-id="798c6-114">Lists deployment scripts in resource group DS-TestRg.</span></span>

### <span data-ttu-id="798c6-115">Exempel 3</span><span class="sxs-lookup"><span data-stu-id="798c6-115">Example 3</span></span>
```powershell
PS C:\> Get-AzDeploymentScript -Name MyDeploymentScript -ResourceGroupName DS-TestRg
```

<span data-ttu-id="798c6-116">Hämtar ett distributions skript med namnet MyDeploymentScript i resurs gruppen DS-TestRG.</span><span class="sxs-lookup"><span data-stu-id="798c6-116">Gets a deployment script with the name MyDeploymentScript in resource group DS-TestRG.</span></span>

### <span data-ttu-id="798c6-117">Exempel 4</span><span class="sxs-lookup"><span data-stu-id="798c6-117">Example 4</span></span>
```powershell
PS C:\> Get-AzDeploymentScript -Id "/subscriptions/{subId}/resourceGroups/{rgName}/providers/Microsoft.Resources/deploymentScripts/{deploymentScriptName}"
```

<span data-ttu-id="798c6-118">Hämtar ett distributions skript med angivet resurs-ID.</span><span class="sxs-lookup"><span data-stu-id="798c6-118">Gets a deployment script with the given resource Id.</span></span> 

## <span data-ttu-id="798c6-119">MALLPARAMETRAR</span><span class="sxs-lookup"><span data-stu-id="798c6-119">PARAMETERS</span></span>

### <span data-ttu-id="798c6-120">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="798c6-120">-DefaultProfile</span></span>
<span data-ttu-id="798c6-121">Autentiseringsuppgifter, konto, klient organisation och abonnemang som används för kommunikation med Azure.</span><span class="sxs-lookup"><span data-stu-id="798c6-121">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

```yaml
Type: IAzureContextContainer
Parameter Sets: (All)
Aliases: AzContext, AzureRmContext, AzureCredential

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="798c6-122">-ID</span><span class="sxs-lookup"><span data-stu-id="798c6-122">-Id</span></span>
<span data-ttu-id="798c6-123">Fullständigt resurs-ID för distributions skriptet.</span><span class="sxs-lookup"><span data-stu-id="798c6-123">The fully qualified resource Id of the deployment script.</span></span>
<span data-ttu-id="798c6-124">Exempel:/subscriptions/{subId}/resourceGroups/{rgName}/providers/Microsoft.Resources/deploymentScripts/{deploymentScriptName}</span><span class="sxs-lookup"><span data-stu-id="798c6-124">Example: /subscriptions/{subId}/resourceGroups/{rgName}/providers/Microsoft.Resources/deploymentScripts/{deploymentScriptName}</span></span>

```yaml
Type: String
Parameter Sets: GetDeploymentScriptByResourceId
Aliases: ResourceId

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="798c6-125">-Namn</span><span class="sxs-lookup"><span data-stu-id="798c6-125">-Name</span></span>
<span data-ttu-id="798c6-126">Namnet på distributions skriptet</span><span class="sxs-lookup"><span data-stu-id="798c6-126">The name of the deployment script</span></span>

```yaml
Type: String
Parameter Sets: GetDeploymentScriptByName
Aliases:

Required: True
Position: 1
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="798c6-127">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="798c6-127">-ResourceGroupName</span></span>
<span data-ttu-id="798c6-128">Namnet på resurs gruppen.</span><span class="sxs-lookup"><span data-stu-id="798c6-128">The name of the resource group.</span></span>

```yaml
Type: String
Parameter Sets: ListDeploymentScript
Aliases:

Required: False
Position: 0
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

```yaml
Type: String
Parameter Sets: GetDeploymentScriptByName
Aliases:

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="798c6-129">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="798c6-129">CommonParameters</span></span>
<span data-ttu-id="798c6-130">Den här cmdleten har stöd för de gemensamma parametrarna:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-disvariable,-utbuffer,-PipelineVariable,-verbose,-WarningAction och-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="798c6-130">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span>
<span data-ttu-id="798c6-131">Mer information finns i about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="798c6-131">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="798c6-132">KOSTNADS</span><span class="sxs-lookup"><span data-stu-id="798c6-132">INPUTS</span></span>

### <span data-ttu-id="798c6-133">System. String</span><span class="sxs-lookup"><span data-stu-id="798c6-133">System.String</span></span>

## <span data-ttu-id="798c6-134">VÄRDEN</span><span class="sxs-lookup"><span data-stu-id="798c6-134">OUTPUTS</span></span>

### <span data-ttu-id="798c6-135">Microsoft.Azure.Commands.ResourceManager.Cmdlets.SdkModels.PsDeploymentScript</span><span class="sxs-lookup"><span data-stu-id="798c6-135">Microsoft.Azure.Commands.ResourceManager.Cmdlets.SdkModels.PsDeploymentScript</span></span>

## <span data-ttu-id="798c6-136">ANMÄRKNINGAR</span><span class="sxs-lookup"><span data-stu-id="798c6-136">NOTES</span></span>

## <span data-ttu-id="798c6-137">RELATERADE LÄNKAR</span><span class="sxs-lookup"><span data-stu-id="798c6-137">RELATED LINKS</span></span>