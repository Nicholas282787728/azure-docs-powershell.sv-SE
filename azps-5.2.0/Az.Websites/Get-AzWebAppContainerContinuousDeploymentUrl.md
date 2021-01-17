---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Websites.dll-Help.xml
Module Name: Az.Websites
online version: https://docs.microsoft.com/en-us/powershell/module/az.websites/get-azwebappcontainercontinuousdeploymenturl
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Websites/Websites/help/Get-AzWebAppContainerContinuousDeploymentUrl.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Websites/Websites/help/Get-AzWebAppContainerContinuousDeploymentUrl.md
ms.openlocfilehash: 2b49b30c06f39561f6d00542dd4ff02df56ee569
ms.sourcegitcommit: 04221336bc9eed46c05ed1e828a6811534d4b4ab
ms.translationtype: MT
ms.contentlocale: sv-SE
ms.lasthandoff: 12/08/2020
ms.locfileid: "98389796"
---
# <span data-ttu-id="2f80d-101">Get-AzWebAppContainerContinuousDeploymentUrl</span><span class="sxs-lookup"><span data-stu-id="2f80d-101">Get-AzWebAppContainerContinuousDeploymentUrl</span></span>

## <span data-ttu-id="2f80d-102">Sammanfattning</span><span class="sxs-lookup"><span data-stu-id="2f80d-102">SYNOPSIS</span></span>
<span data-ttu-id="2f80d-103">Get-AzWebAppContainerContinuousDeploymentUrl returnerar URL för kontinuerlig distribution av behållare</span><span class="sxs-lookup"><span data-stu-id="2f80d-103">Get-AzWebAppContainerContinuousDeploymentUrl will return container continuous deployment url</span></span>

## <span data-ttu-id="2f80d-104">FRÅGESYNTAXEN</span><span class="sxs-lookup"><span data-stu-id="2f80d-104">SYNTAX</span></span>

### <span data-ttu-id="2f80d-105">S1 (standard)</span><span class="sxs-lookup"><span data-stu-id="2f80d-105">S1 (Default)</span></span>
```
Get-AzWebAppContainerContinuousDeploymentUrl [[-SlotName] <String>] [-ResourceGroupName] <String>
 [-Name] <String> [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="2f80d-106">S2</span><span class="sxs-lookup"><span data-stu-id="2f80d-106">S2</span></span>
```
Get-AzWebAppContainerContinuousDeploymentUrl [-WebApp] <PSSite> [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

## <span data-ttu-id="2f80d-107">PROBLEMBESKRIVNING</span><span class="sxs-lookup"><span data-stu-id="2f80d-107">DESCRIPTION</span></span>
<span data-ttu-id="2f80d-108">Get-AzWebAppContainerContinuousDeploymentUrl returnerar URL för kontinuerlig distribution av behållare</span><span class="sxs-lookup"><span data-stu-id="2f80d-108">Get-AzWebAppContainerContinuousDeploymentUrl will return container continuous deployment url</span></span>

## <span data-ttu-id="2f80d-109">BESKRIVS</span><span class="sxs-lookup"><span data-stu-id="2f80d-109">EXAMPLES</span></span>

### <span data-ttu-id="2f80d-110">Exempel 1</span><span class="sxs-lookup"><span data-stu-id="2f80d-110">Example 1</span></span>
```
PS C:\> Get-AzWebAppContainerContinuousDeploymentUrl -ResourceGroupName "Default-Web-WestUS" -Name "ContosoASP"
```

<span data-ttu-id="2f80d-111">Det här kommandot returnerar URL för kontinuerlig distribution av behållare.</span><span class="sxs-lookup"><span data-stu-id="2f80d-111">This command will return container continuous deployment url.</span></span>

## <span data-ttu-id="2f80d-112">MALLPARAMETRAR</span><span class="sxs-lookup"><span data-stu-id="2f80d-112">PARAMETERS</span></span>

### <span data-ttu-id="2f80d-113">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="2f80d-113">-DefaultProfile</span></span>
<span data-ttu-id="2f80d-114">Autentiseringsuppgifter, konto, klient organisation och abonnemang som används för kommunikation med Azure.</span><span class="sxs-lookup"><span data-stu-id="2f80d-114">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="2f80d-115">-Namn</span><span class="sxs-lookup"><span data-stu-id="2f80d-115">-Name</span></span>
<span data-ttu-id="2f80d-116">Namnet på webb programmet.</span><span class="sxs-lookup"><span data-stu-id="2f80d-116">The name of the web app.</span></span>

```yaml
Type: System.String
Parameter Sets: S1
Aliases:

Required: True
Position: 1
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="2f80d-117">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="2f80d-117">-ResourceGroupName</span></span>
<span data-ttu-id="2f80d-118">Namnet på resurs gruppen.</span><span class="sxs-lookup"><span data-stu-id="2f80d-118">The name of the resource group.</span></span>

```yaml
Type: System.String
Parameter Sets: S1
Aliases:

Required: True
Position: 0
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="2f80d-119">-SlotName</span><span class="sxs-lookup"><span data-stu-id="2f80d-119">-SlotName</span></span>
<span data-ttu-id="2f80d-120">Namnet på Web App-platsen.</span><span class="sxs-lookup"><span data-stu-id="2f80d-120">The name of the web app slot.</span></span>

```yaml
Type: System.String
Parameter Sets: S1
Aliases:

Required: False
Position: 1
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="2f80d-121">-WebApp</span><span class="sxs-lookup"><span data-stu-id="2f80d-121">-WebApp</span></span>
<span data-ttu-id="2f80d-122">Web App-objekt</span><span class="sxs-lookup"><span data-stu-id="2f80d-122">The web app object</span></span>

```yaml
Type: Microsoft.Azure.Commands.WebApps.Models.PSSite
Parameter Sets: S2
Aliases:

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="2f80d-123">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="2f80d-123">CommonParameters</span></span>
<span data-ttu-id="2f80d-124">Den här cmdleten har stöd för de gemensamma parametrarna:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-disvariable,-utbuffer,-PipelineVariable,-verbose,-WarningAction och-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="2f80d-124">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="2f80d-125">Mer information finns i about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="2f80d-125">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="2f80d-126">KOSTNADS</span><span class="sxs-lookup"><span data-stu-id="2f80d-126">INPUTS</span></span>

### <span data-ttu-id="2f80d-127">System. String</span><span class="sxs-lookup"><span data-stu-id="2f80d-127">System.String</span></span>

### <span data-ttu-id="2f80d-128">Microsoft. Azure. commands. webapps. Models. PSSite</span><span class="sxs-lookup"><span data-stu-id="2f80d-128">Microsoft.Azure.Commands.WebApps.Models.PSSite</span></span>

## <span data-ttu-id="2f80d-129">VÄRDEN</span><span class="sxs-lookup"><span data-stu-id="2f80d-129">OUTPUTS</span></span>

### <span data-ttu-id="2f80d-130">System. String</span><span class="sxs-lookup"><span data-stu-id="2f80d-130">System.String</span></span>

## <span data-ttu-id="2f80d-131">ANMÄRKNINGAR</span><span class="sxs-lookup"><span data-stu-id="2f80d-131">NOTES</span></span>

## <span data-ttu-id="2f80d-132">RELATERADE LÄNKAR</span><span class="sxs-lookup"><span data-stu-id="2f80d-132">RELATED LINKS</span></span>
