---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Websites.dll-Help.xml
Module Name: Az.Websites
ms.assetid: 0FDDDEE1-CEAD-46DA-A7EB-EE477ED59749
online version: https://docs.microsoft.com/en-us/powershell/module/az.websites/start-azwebappslot
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Websites/Websites/help/Start-AzWebAppSlot.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Websites/Websites/help/Start-AzWebAppSlot.md
ms.openlocfilehash: 4425c344fb0c9e0e3441c172915be11002ee8b1b
ms.sourcegitcommit: b4a38bcb0501a9016a4998efd377aa75d3ef9ce8
ms.translationtype: MT
ms.contentlocale: sv-SE
ms.lasthandoff: 10/27/2020
ms.locfileid: "94271181"
---
# <span data-ttu-id="9702b-101">Start-AzWebAppSlot</span><span class="sxs-lookup"><span data-stu-id="9702b-101">Start-AzWebAppSlot</span></span>

## <span data-ttu-id="9702b-102">Sammanfattning</span><span class="sxs-lookup"><span data-stu-id="9702b-102">SYNOPSIS</span></span>
<span data-ttu-id="9702b-103">Startar en Azure Web App-plats.</span><span class="sxs-lookup"><span data-stu-id="9702b-103">Starts an Azure Web App slot.</span></span>

## <span data-ttu-id="9702b-104">FRÅGESYNTAXEN</span><span class="sxs-lookup"><span data-stu-id="9702b-104">SYNTAX</span></span>

### <span data-ttu-id="9702b-105">S</span><span class="sxs-lookup"><span data-stu-id="9702b-105">S1</span></span>
```
Start-AzWebAppSlot [-ResourceGroupName] <String> [-Name] <String> [-Slot] <String>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="9702b-106">S2</span><span class="sxs-lookup"><span data-stu-id="9702b-106">S2</span></span>
```
Start-AzWebAppSlot [-WebApp] <PSSite> [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="9702b-107">PROBLEMBESKRIVNING</span><span class="sxs-lookup"><span data-stu-id="9702b-107">DESCRIPTION</span></span>
<span data-ttu-id="9702b-108">Cmdleten **Start-AzWebAppSlot** startar en Azure Web App-plats.</span><span class="sxs-lookup"><span data-stu-id="9702b-108">The **Start-AzWebAppSlot** cmdlet starts an Azure Web App Slot.</span></span>

## <span data-ttu-id="9702b-109">BESKRIVS</span><span class="sxs-lookup"><span data-stu-id="9702b-109">EXAMPLES</span></span>

### <span data-ttu-id="9702b-110">Exempel 1</span><span class="sxs-lookup"><span data-stu-id="9702b-110">Example 1</span></span>
```
PS C:\>Start-AzWebAppSlot -ResourceGroupName "Default-Web-WestUS" -Name "ContosoWebApp" -Slot "Slot001"
```

<span data-ttu-id="9702b-111">Det här kommandot startar facket som heter Slot001 som hör till webb programmet som heter ContosoWebApp och som tillhör resurs gruppen som heter default-West-väst.</span><span class="sxs-lookup"><span data-stu-id="9702b-111">This command starts the Slot named Slot001 pertaining to the Web App named ContosoWebApp that belongs to the resource group named Default-Web-WestUS.</span></span>

## <span data-ttu-id="9702b-112">MALLPARAMETRAR</span><span class="sxs-lookup"><span data-stu-id="9702b-112">PARAMETERS</span></span>

### <span data-ttu-id="9702b-113">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="9702b-113">-DefaultProfile</span></span>
<span data-ttu-id="9702b-114">Autentiseringsuppgifter, konto, klient organisation och abonnemang som används för kommunikation med Azure.</span><span class="sxs-lookup"><span data-stu-id="9702b-114">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="9702b-115">-Namn</span><span class="sxs-lookup"><span data-stu-id="9702b-115">-Name</span></span>
<span data-ttu-id="9702b-116">WebApp-namn</span><span class="sxs-lookup"><span data-stu-id="9702b-116">WebApp Name</span></span>

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

### <span data-ttu-id="9702b-117">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="9702b-117">-ResourceGroupName</span></span>
<span data-ttu-id="9702b-118">Resurs grupps namn</span><span class="sxs-lookup"><span data-stu-id="9702b-118">Resource Group Name</span></span>

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

### <span data-ttu-id="9702b-119">-Plats</span><span class="sxs-lookup"><span data-stu-id="9702b-119">-Slot</span></span>
<span data-ttu-id="9702b-120">WebApp-slot</span><span class="sxs-lookup"><span data-stu-id="9702b-120">WebApp Slot Name</span></span>

```yaml
Type: System.String
Parameter Sets: S1
Aliases:

Required: True
Position: 2
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="9702b-121">-WebApp</span><span class="sxs-lookup"><span data-stu-id="9702b-121">-WebApp</span></span>
<span data-ttu-id="9702b-122">WebApp-objekt</span><span class="sxs-lookup"><span data-stu-id="9702b-122">WebApp Object</span></span>

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

### <span data-ttu-id="9702b-123">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="9702b-123">CommonParameters</span></span>
<span data-ttu-id="9702b-124">Den här cmdleten har stöd för de gemensamma parametrarna:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-disvariable,-utbuffer,-PipelineVariable,-verbose,-WarningAction och-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="9702b-124">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="9702b-125">Mer information finns i about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="9702b-125">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="9702b-126">KOSTNADS</span><span class="sxs-lookup"><span data-stu-id="9702b-126">INPUTS</span></span>

### <span data-ttu-id="9702b-127">System. String</span><span class="sxs-lookup"><span data-stu-id="9702b-127">System.String</span></span>

### <span data-ttu-id="9702b-128">Microsoft. Azure. commands. webapps. Models. PSSite</span><span class="sxs-lookup"><span data-stu-id="9702b-128">Microsoft.Azure.Commands.WebApps.Models.PSSite</span></span>

## <span data-ttu-id="9702b-129">VÄRDEN</span><span class="sxs-lookup"><span data-stu-id="9702b-129">OUTPUTS</span></span>

### <span data-ttu-id="9702b-130">Microsoft. Azure. commands. webapps. Models. PSSite</span><span class="sxs-lookup"><span data-stu-id="9702b-130">Microsoft.Azure.Commands.WebApps.Models.PSSite</span></span>

## <span data-ttu-id="9702b-131">ANMÄRKNINGAR</span><span class="sxs-lookup"><span data-stu-id="9702b-131">NOTES</span></span>

## <span data-ttu-id="9702b-132">RELATERADE LÄNKAR</span><span class="sxs-lookup"><span data-stu-id="9702b-132">RELATED LINKS</span></span>

[<span data-ttu-id="9702b-133">Get-AzWebAppSlot</span><span class="sxs-lookup"><span data-stu-id="9702b-133">Get-AzWebAppSlot</span></span>](./Get-AzWebAppSlot.md)

[<span data-ttu-id="9702b-134">New-AzWebAppSlot</span><span class="sxs-lookup"><span data-stu-id="9702b-134">New-AzWebAppSlot</span></span>](./New-AzWebAppSlot.md)

[<span data-ttu-id="9702b-135">Remove-AzWebAppSlot</span><span class="sxs-lookup"><span data-stu-id="9702b-135">Remove-AzWebAppSlot</span></span>](./Remove-AzWebAppSlot.md)

[<span data-ttu-id="9702b-136">Restart-AzWebAppSlot</span><span class="sxs-lookup"><span data-stu-id="9702b-136">Restart-AzWebAppSlot</span></span>](./Restart-AzWebAppSlot.md)

[<span data-ttu-id="9702b-137">Set-AzWebAppSlot</span><span class="sxs-lookup"><span data-stu-id="9702b-137">Set-AzWebAppSlot</span></span>](./Set-AzWebAppSlot.md)

[<span data-ttu-id="9702b-138">Stopp-AzWebAppSlot</span><span class="sxs-lookup"><span data-stu-id="9702b-138">Stop-AzWebAppSlot</span></span>](./Stop-AzWebAppSlot.md)

[<span data-ttu-id="9702b-139">Get-AzWebApp</span><span class="sxs-lookup"><span data-stu-id="9702b-139">Get-AzWebApp</span></span>](./Get-AzWebApp.md)