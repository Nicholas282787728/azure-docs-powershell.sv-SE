---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Websites.dll-Help.xml
Module Name: Az.Websites
ms.assetid: 86E0D477-DD32-49BD-82E7-1CF191E4F612
online version: https://docs.microsoft.com/en-us/powershell/module/az.websites/stop-azwebappslot
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Websites/Websites/help/Stop-AzWebAppSlot.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Websites/Websites/help/Stop-AzWebAppSlot.md
ms.openlocfilehash: 455a1735df128ee84d99adb6461c602a7b1dbbdf
ms.sourcegitcommit: 4d2c178cd6df9151877b08d54c1f4a228dbec9d1
ms.translationtype: MT
ms.contentlocale: sv-SE
ms.lasthandoff: 01/29/2020
ms.locfileid: "93746010"
---
# <span data-ttu-id="da900-101">Stop-AzWebAppSlot</span><span class="sxs-lookup"><span data-stu-id="da900-101">Stop-AzWebAppSlot</span></span>

## <span data-ttu-id="da900-102">Sammanfattning</span><span class="sxs-lookup"><span data-stu-id="da900-102">SYNOPSIS</span></span>
<span data-ttu-id="da900-103">Stoppar en Azure Web App-plats.</span><span class="sxs-lookup"><span data-stu-id="da900-103">Stops an Azure Web App slot.</span></span>

## <span data-ttu-id="da900-104">FRÅGESYNTAXEN</span><span class="sxs-lookup"><span data-stu-id="da900-104">SYNTAX</span></span>

### <span data-ttu-id="da900-105">S</span><span class="sxs-lookup"><span data-stu-id="da900-105">S1</span></span>
```
Stop-AzWebAppSlot [-ResourceGroupName] <String> [-Name] <String> [-Slot] <String>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="da900-106">S2</span><span class="sxs-lookup"><span data-stu-id="da900-106">S2</span></span>
```
Stop-AzWebAppSlot [-WebApp] <PSSite> [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="da900-107">PROBLEMBESKRIVNING</span><span class="sxs-lookup"><span data-stu-id="da900-107">DESCRIPTION</span></span>
<span data-ttu-id="da900-108">Cmdleten **Stop-AzWebAppSlot** stoppar en Azure Web App-plats.</span><span class="sxs-lookup"><span data-stu-id="da900-108">The **Stop-AzWebAppSlot** cmdlet stops an Azure Web App Slot.</span></span>

## <span data-ttu-id="da900-109">BESKRIVS</span><span class="sxs-lookup"><span data-stu-id="da900-109">EXAMPLES</span></span>

### <span data-ttu-id="da900-110">Exempel 1</span><span class="sxs-lookup"><span data-stu-id="da900-110">Example 1</span></span>
```
PS C:\>Stop-AzWebAppSlot -ResourceGroupName "Default-Web-WestUS" -Name "ContosoWebApp" -Slot "Slot001"
```

<span data-ttu-id="da900-111">Det här kommandot stoppar fack Slot001 för webb programmet som heter ContosoWebApp som tillhör resurs gruppen med namnet default-Web-West.</span><span class="sxs-lookup"><span data-stu-id="da900-111">This command stops the slot Slot001 pertaining to the Web App named ContosoWebApp that belongs to the resource group named Default-Web-WestUS.</span></span>

## <span data-ttu-id="da900-112">MALLPARAMETRAR</span><span class="sxs-lookup"><span data-stu-id="da900-112">PARAMETERS</span></span>

### <span data-ttu-id="da900-113">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="da900-113">-DefaultProfile</span></span>
<span data-ttu-id="da900-114">Autentiseringsuppgifter, konto, klient organisation och abonnemang som används för kommunikation med Azure.</span><span class="sxs-lookup"><span data-stu-id="da900-114">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="da900-115">-Namn</span><span class="sxs-lookup"><span data-stu-id="da900-115">-Name</span></span>
<span data-ttu-id="da900-116">WebApp-namn</span><span class="sxs-lookup"><span data-stu-id="da900-116">WebApp Name</span></span>

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

### <span data-ttu-id="da900-117">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="da900-117">-ResourceGroupName</span></span>
<span data-ttu-id="da900-118">Resurs grupps namn</span><span class="sxs-lookup"><span data-stu-id="da900-118">Resource Group Name</span></span>

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

### <span data-ttu-id="da900-119">-Plats</span><span class="sxs-lookup"><span data-stu-id="da900-119">-Slot</span></span>
<span data-ttu-id="da900-120">WebApp-slot</span><span class="sxs-lookup"><span data-stu-id="da900-120">WebApp Slot Name</span></span>

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

### <span data-ttu-id="da900-121">-WebApp</span><span class="sxs-lookup"><span data-stu-id="da900-121">-WebApp</span></span>
<span data-ttu-id="da900-122">WebApp-objekt</span><span class="sxs-lookup"><span data-stu-id="da900-122">WebApp Object</span></span>

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

### <span data-ttu-id="da900-123">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="da900-123">CommonParameters</span></span>
<span data-ttu-id="da900-124">Den här cmdleten har stöd för de gemensamma parametrarna:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-disvariable,-utbuffer,-PipelineVariable,-verbose,-WarningAction och-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="da900-124">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="da900-125">Mer information finns i about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="da900-125">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="da900-126">KOSTNADS</span><span class="sxs-lookup"><span data-stu-id="da900-126">INPUTS</span></span>

### <span data-ttu-id="da900-127">System. String</span><span class="sxs-lookup"><span data-stu-id="da900-127">System.String</span></span>

### <span data-ttu-id="da900-128">Microsoft. Azure. commands. webapps. Models. PSSite</span><span class="sxs-lookup"><span data-stu-id="da900-128">Microsoft.Azure.Commands.WebApps.Models.PSSite</span></span>

## <span data-ttu-id="da900-129">VÄRDEN</span><span class="sxs-lookup"><span data-stu-id="da900-129">OUTPUTS</span></span>

### <span data-ttu-id="da900-130">Microsoft. Azure. commands. webapps. Models. PSSite</span><span class="sxs-lookup"><span data-stu-id="da900-130">Microsoft.Azure.Commands.WebApps.Models.PSSite</span></span>

## <span data-ttu-id="da900-131">ANMÄRKNINGAR</span><span class="sxs-lookup"><span data-stu-id="da900-131">NOTES</span></span>

## <span data-ttu-id="da900-132">RELATERADE LÄNKAR</span><span class="sxs-lookup"><span data-stu-id="da900-132">RELATED LINKS</span></span>
