---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Websites.dll-Help.xml
Module Name: Az.Websites
online version: https://docs.microsoft.com/en-us/powershell/module/az.websites/get-azwebappcontainercontinuousdeploymenturl
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Websites/Websites/help/Get-AzWebAppContainerContinuousDeploymentUrl.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Websites/Websites/help/Get-AzWebAppContainerContinuousDeploymentUrl.md
ms.openlocfilehash: 2b49b30c06f39561f6d00542dd4ff02df56ee569
ms.sourcegitcommit: b4a38bcb0501a9016a4998efd377aa75d3ef9ce8
ms.translationtype: MT
ms.contentlocale: sv-SE
ms.lasthandoff: 10/27/2020
ms.locfileid: "94323484"
---
# <span data-ttu-id="76f42-101">Get-AzWebAppContainerContinuousDeploymentUrl</span><span class="sxs-lookup"><span data-stu-id="76f42-101">Get-AzWebAppContainerContinuousDeploymentUrl</span></span>

## <span data-ttu-id="76f42-102">Sammanfattning</span><span class="sxs-lookup"><span data-stu-id="76f42-102">SYNOPSIS</span></span>
<span data-ttu-id="76f42-103">Get-AzWebAppContainerContinuousDeploymentUrl returnerar URL för kontinuerlig distribution av behållare</span><span class="sxs-lookup"><span data-stu-id="76f42-103">Get-AzWebAppContainerContinuousDeploymentUrl will return container continuous deployment url</span></span>

## <span data-ttu-id="76f42-104">FRÅGESYNTAXEN</span><span class="sxs-lookup"><span data-stu-id="76f42-104">SYNTAX</span></span>

### <span data-ttu-id="76f42-105">S1 (standard)</span><span class="sxs-lookup"><span data-stu-id="76f42-105">S1 (Default)</span></span>
```
Get-AzWebAppContainerContinuousDeploymentUrl [[-SlotName] <String>] [-ResourceGroupName] <String>
 [-Name] <String> [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="76f42-106">S2</span><span class="sxs-lookup"><span data-stu-id="76f42-106">S2</span></span>
```
Get-AzWebAppContainerContinuousDeploymentUrl [-WebApp] <PSSite> [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

## <span data-ttu-id="76f42-107">PROBLEMBESKRIVNING</span><span class="sxs-lookup"><span data-stu-id="76f42-107">DESCRIPTION</span></span>
<span data-ttu-id="76f42-108">Get-AzWebAppContainerContinuousDeploymentUrl returnerar URL för kontinuerlig distribution av behållare</span><span class="sxs-lookup"><span data-stu-id="76f42-108">Get-AzWebAppContainerContinuousDeploymentUrl will return container continuous deployment url</span></span>

## <span data-ttu-id="76f42-109">BESKRIVS</span><span class="sxs-lookup"><span data-stu-id="76f42-109">EXAMPLES</span></span>

### <span data-ttu-id="76f42-110">Exempel 1</span><span class="sxs-lookup"><span data-stu-id="76f42-110">Example 1</span></span>
```
PS C:\> Get-AzWebAppContainerContinuousDeploymentUrl -ResourceGroupName "Default-Web-WestUS" -Name "ContosoASP"
```

<span data-ttu-id="76f42-111">Det här kommandot returnerar URL för kontinuerlig distribution av behållare.</span><span class="sxs-lookup"><span data-stu-id="76f42-111">This command will return container continuous deployment url.</span></span>

## <span data-ttu-id="76f42-112">MALLPARAMETRAR</span><span class="sxs-lookup"><span data-stu-id="76f42-112">PARAMETERS</span></span>

### <span data-ttu-id="76f42-113">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="76f42-113">-DefaultProfile</span></span>
<span data-ttu-id="76f42-114">Autentiseringsuppgifter, konto, klient organisation och abonnemang som används för kommunikation med Azure.</span><span class="sxs-lookup"><span data-stu-id="76f42-114">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="76f42-115">-Namn</span><span class="sxs-lookup"><span data-stu-id="76f42-115">-Name</span></span>
<span data-ttu-id="76f42-116">Namnet på webb programmet.</span><span class="sxs-lookup"><span data-stu-id="76f42-116">The name of the web app.</span></span>

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

### <span data-ttu-id="76f42-117">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="76f42-117">-ResourceGroupName</span></span>
<span data-ttu-id="76f42-118">Namnet på resurs gruppen.</span><span class="sxs-lookup"><span data-stu-id="76f42-118">The name of the resource group.</span></span>

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

### <span data-ttu-id="76f42-119">-SlotName</span><span class="sxs-lookup"><span data-stu-id="76f42-119">-SlotName</span></span>
<span data-ttu-id="76f42-120">Namnet på Web App-platsen.</span><span class="sxs-lookup"><span data-stu-id="76f42-120">The name of the web app slot.</span></span>

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

### <span data-ttu-id="76f42-121">-WebApp</span><span class="sxs-lookup"><span data-stu-id="76f42-121">-WebApp</span></span>
<span data-ttu-id="76f42-122">Web App-objekt</span><span class="sxs-lookup"><span data-stu-id="76f42-122">The web app object</span></span>

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

### <span data-ttu-id="76f42-123">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="76f42-123">CommonParameters</span></span>
<span data-ttu-id="76f42-124">Den här cmdleten har stöd för de gemensamma parametrarna:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-disvariable,-utbuffer,-PipelineVariable,-verbose,-WarningAction och-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="76f42-124">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="76f42-125">Mer information finns i about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="76f42-125">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="76f42-126">KOSTNADS</span><span class="sxs-lookup"><span data-stu-id="76f42-126">INPUTS</span></span>

### <span data-ttu-id="76f42-127">System. String</span><span class="sxs-lookup"><span data-stu-id="76f42-127">System.String</span></span>

### <span data-ttu-id="76f42-128">Microsoft. Azure. commands. webapps. Models. PSSite</span><span class="sxs-lookup"><span data-stu-id="76f42-128">Microsoft.Azure.Commands.WebApps.Models.PSSite</span></span>

## <span data-ttu-id="76f42-129">VÄRDEN</span><span class="sxs-lookup"><span data-stu-id="76f42-129">OUTPUTS</span></span>

### <span data-ttu-id="76f42-130">System. String</span><span class="sxs-lookup"><span data-stu-id="76f42-130">System.String</span></span>

## <span data-ttu-id="76f42-131">ANMÄRKNINGAR</span><span class="sxs-lookup"><span data-stu-id="76f42-131">NOTES</span></span>

## <span data-ttu-id="76f42-132">RELATERADE LÄNKAR</span><span class="sxs-lookup"><span data-stu-id="76f42-132">RELATED LINKS</span></span>
