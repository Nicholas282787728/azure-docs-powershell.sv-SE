---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Aks.dll-Help.xml
Module Name: Az.Aks
online version: https://docs.microsoft.com/en-us/powershell/module/az.aks/install-azakskubectl
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Aks/Aks/help/Install-AzAksKubectl.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Aks/Aks/help/Install-AzAksKubectl.md
ms.openlocfilehash: 746efc579e1977e54a1898bbe183d951c3d9c21f
ms.sourcegitcommit: 04221336bc9eed46c05ed1e828a6811534d4b4ab
ms.translationtype: MT
ms.contentlocale: sv-SE
ms.lasthandoff: 12/08/2020
ms.locfileid: "98405555"
---
# <span data-ttu-id="e8371-101">Install-AzAksKubectl</span><span class="sxs-lookup"><span data-stu-id="e8371-101">Install-AzAksKubectl</span></span>

## <span data-ttu-id="e8371-102">Sammanfattning</span><span class="sxs-lookup"><span data-stu-id="e8371-102">SYNOPSIS</span></span>
<span data-ttu-id="e8371-103">Ladda ned och installera kubectl, kommando rads verktyget Kubernetes.</span><span class="sxs-lookup"><span data-stu-id="e8371-103">Download and install kubectl, the Kubernetes command-line tool.</span></span>

## <span data-ttu-id="e8371-104">FRÅGESYNTAXEN</span><span class="sxs-lookup"><span data-stu-id="e8371-104">SYNTAX</span></span>

```
Install-AzAksKubectl [-Destination <String>] [-Version <String>] [-DownloadFromMirror] [-PassThru] [-AsJob]
 [-Force] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="e8371-105">PROBLEMBESKRIVNING</span><span class="sxs-lookup"><span data-stu-id="e8371-105">DESCRIPTION</span></span>
<span data-ttu-id="e8371-106">Ladda ned och installera kubectl, kommando rads verktyget Kubernetes.</span><span class="sxs-lookup"><span data-stu-id="e8371-106">Download and install kubectl, the Kubernetes command-line tool.</span></span>

## <span data-ttu-id="e8371-107">BESKRIVS</span><span class="sxs-lookup"><span data-stu-id="e8371-107">EXAMPLES</span></span>

### <span data-ttu-id="e8371-108">Ladda ned och installera den senaste versionen av kubectl</span><span class="sxs-lookup"><span data-stu-id="e8371-108">Download and install latest version of kubectl</span></span>
```powershell
PS C:\> Install-AzAksKubectl -Version latest
```

## <span data-ttu-id="e8371-109">MALLPARAMETRAR</span><span class="sxs-lookup"><span data-stu-id="e8371-109">PARAMETERS</span></span>

### <span data-ttu-id="e8371-110">-AsJob</span><span class="sxs-lookup"><span data-stu-id="e8371-110">-AsJob</span></span>
<span data-ttu-id="e8371-111">Kör cmdlet i bakgrunden</span><span class="sxs-lookup"><span data-stu-id="e8371-111">Run cmdlet in the background</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="e8371-112">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="e8371-112">-DefaultProfile</span></span>
<span data-ttu-id="e8371-113">Autentiseringsuppgifter, konto, klient organisation och abonnemang som används för kommunikation med Azure.</span><span class="sxs-lookup"><span data-stu-id="e8371-113">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="e8371-114">-Mål</span><span class="sxs-lookup"><span data-stu-id="e8371-114">-Destination</span></span>
<span data-ttu-id="e8371-115">Sökväg där du vill installera kubectl.</span><span class="sxs-lookup"><span data-stu-id="e8371-115">Path at which to install kubectl.</span></span>
<span data-ttu-id="e8371-116">Standard för installation till ~/.Azure-kubectl/</span><span class="sxs-lookup"><span data-stu-id="e8371-116">Default to install into ~/.azure-kubectl/</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="e8371-117">-DownloadFromMirror</span><span class="sxs-lookup"><span data-stu-id="e8371-117">-DownloadFromMirror</span></span>
<span data-ttu-id="e8371-118">Ladda ned från spegel webbplats: https://mirror.azure.cn/kubernetes/kubectl/</span><span class="sxs-lookup"><span data-stu-id="e8371-118">Download from mirror site : https://mirror.azure.cn/kubernetes/kubectl/</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="e8371-119">-Force</span><span class="sxs-lookup"><span data-stu-id="e8371-119">-Force</span></span>
<span data-ttu-id="e8371-120">Skriv över befintlig kubectl utan fråga</span><span class="sxs-lookup"><span data-stu-id="e8371-120">Overwrite existing kubectl without prompt</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="e8371-121">-PassThru</span><span class="sxs-lookup"><span data-stu-id="e8371-121">-PassThru</span></span>
<span data-ttu-id="e8371-122">{{Fill PassThru Description}}</span><span class="sxs-lookup"><span data-stu-id="e8371-122">{{ Fill PassThru Description }}</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="e8371-123">-Version</span><span class="sxs-lookup"><span data-stu-id="e8371-123">-Version</span></span>
<span data-ttu-id="e8371-124">Version av kubectl som ska installeras, t. ex.</span><span class="sxs-lookup"><span data-stu-id="e8371-124">Version of kubectl to install, e.g. 'v1.17.2'.</span></span>
<span data-ttu-id="e8371-125">Standardvärde: senaste</span><span class="sxs-lookup"><span data-stu-id="e8371-125">Default value: Latest</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="e8371-126">-Bekräfta</span><span class="sxs-lookup"><span data-stu-id="e8371-126">-Confirm</span></span>
<span data-ttu-id="e8371-127">Du uppmanas att bekräfta innan du kör cmdleten.</span><span class="sxs-lookup"><span data-stu-id="e8371-127">Prompts you for confirmation before running the cmdlet.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases: cf

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="e8371-128">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="e8371-128">-WhatIf</span></span>
<span data-ttu-id="e8371-129">Visar vad som händer om cmdleten körs.</span><span class="sxs-lookup"><span data-stu-id="e8371-129">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="e8371-130">Cmdleten körs inte.</span><span class="sxs-lookup"><span data-stu-id="e8371-130">The cmdlet is not run.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases: wi

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="e8371-131">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="e8371-131">CommonParameters</span></span>
<span data-ttu-id="e8371-132">Den här cmdleten har stöd för de gemensamma parametrarna:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-disvariable,-utbuffer,-PipelineVariable,-verbose,-WarningAction och-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="e8371-132">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="e8371-133">Mer information finns i [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="e8371-133">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="e8371-134">KOSTNADS</span><span class="sxs-lookup"><span data-stu-id="e8371-134">INPUTS</span></span>

### <span data-ttu-id="e8371-135">Ingen</span><span class="sxs-lookup"><span data-stu-id="e8371-135">None</span></span>

## <span data-ttu-id="e8371-136">VÄRDEN</span><span class="sxs-lookup"><span data-stu-id="e8371-136">OUTPUTS</span></span>

### <span data-ttu-id="e8371-137">System. Boolean</span><span class="sxs-lookup"><span data-stu-id="e8371-137">System.Boolean</span></span>

## <span data-ttu-id="e8371-138">ANMÄRKNINGAR</span><span class="sxs-lookup"><span data-stu-id="e8371-138">NOTES</span></span>

## <span data-ttu-id="e8371-139">RELATERADE LÄNKAR</span><span class="sxs-lookup"><span data-stu-id="e8371-139">RELATED LINKS</span></span>
