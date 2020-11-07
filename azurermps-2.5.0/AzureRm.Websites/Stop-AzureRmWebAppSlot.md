---
external help file: Microsoft.Azure.Commands.Websites.dll-Help.xml
Module Name: AzureRM.WebSites
ms.assetid: 86E0D477-DD32-49BD-82E7-1CF191E4F612
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.websites/stop-azurermwebappslot
schema: 2.0.0
ms.openlocfilehash: c59e40765fc5da07c5d079e3b5abd6224a8cbc5f
ms.sourcegitcommit: b9b2dea3441d1532a5564ddca3dced45424fe2d6
ms.translationtype: MT
ms.contentlocale: sv-SE
ms.lasthandoff: 08/15/2020
ms.locfileid: "93930434"
---
# <span data-ttu-id="77603-101">Stop-AzureRmWebAppSlot</span><span class="sxs-lookup"><span data-stu-id="77603-101">Stop-AzureRmWebAppSlot</span></span>

## <span data-ttu-id="77603-102">Sammanfattning</span><span class="sxs-lookup"><span data-stu-id="77603-102">SYNOPSIS</span></span>
<span data-ttu-id="77603-103">Stoppar en Azure Web App-plats.</span><span class="sxs-lookup"><span data-stu-id="77603-103">Stops an Azure Web App slot.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="77603-104">FRÅGESYNTAXEN</span><span class="sxs-lookup"><span data-stu-id="77603-104">SYNTAX</span></span>

### <span data-ttu-id="77603-105">S</span><span class="sxs-lookup"><span data-stu-id="77603-105">S1</span></span>
```
Stop-AzureRmWebAppSlot [-ResourceGroupName] <String> [-Name] <String> [-Slot] <String>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="77603-106">S2</span><span class="sxs-lookup"><span data-stu-id="77603-106">S2</span></span>
```
Stop-AzureRmWebAppSlot [-WebApp] <Site> [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="77603-107">PROBLEMBESKRIVNING</span><span class="sxs-lookup"><span data-stu-id="77603-107">DESCRIPTION</span></span>
<span data-ttu-id="77603-108">Cmdleten **Stop-AzureRmWebAppSlot** stoppar en Azure Web App-plats.</span><span class="sxs-lookup"><span data-stu-id="77603-108">The **Stop-AzureRmWebAppSlot** cmdlet stops an Azure Web App Slot.</span></span>

## <span data-ttu-id="77603-109">BESKRIVS</span><span class="sxs-lookup"><span data-stu-id="77603-109">EXAMPLES</span></span>

### <span data-ttu-id="77603-110">Exempel 1</span><span class="sxs-lookup"><span data-stu-id="77603-110">Example 1</span></span>
```
PS C:\>Stop-AzureRmWebAppSlot -ResourceGroupName "Default-Web-WestUS" -Name "ContosoWebApp" -Slot "Slot001"
```

<span data-ttu-id="77603-111">Det här kommandot stoppar fack Slot001 för webb programmet som heter ContosoWebApp som tillhör resurs gruppen med namnet default-Web-West.</span><span class="sxs-lookup"><span data-stu-id="77603-111">This command stops the slot Slot001 pertaining to the Web App named ContosoWebApp that belongs to the resource group named Default-Web-WestUS.</span></span>

## <span data-ttu-id="77603-112">MALLPARAMETRAR</span><span class="sxs-lookup"><span data-stu-id="77603-112">PARAMETERS</span></span>

### <span data-ttu-id="77603-113">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="77603-113">-DefaultProfile</span></span>
<span data-ttu-id="77603-114">Autentiseringsuppgifter, konto, klient organisation och abonnemang som används för kommunikation med Azure.</span><span class="sxs-lookup"><span data-stu-id="77603-114">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="77603-115">-Namn</span><span class="sxs-lookup"><span data-stu-id="77603-115">-Name</span></span>
<span data-ttu-id="77603-116">WebApp-namn</span><span class="sxs-lookup"><span data-stu-id="77603-116">WebApp Name</span></span>

```yaml
Type: String
Parameter Sets: S1
Aliases: 

Required: True
Position: 1
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="77603-117">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="77603-117">-ResourceGroupName</span></span>
<span data-ttu-id="77603-118">Resurs grupps namn</span><span class="sxs-lookup"><span data-stu-id="77603-118">Resource Group Name</span></span>

```yaml
Type: String
Parameter Sets: S1
Aliases: 

Required: True
Position: 0
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="77603-119">-Plats</span><span class="sxs-lookup"><span data-stu-id="77603-119">-Slot</span></span>
<span data-ttu-id="77603-120">WebApp-slot</span><span class="sxs-lookup"><span data-stu-id="77603-120">WebApp Slot Name</span></span>

```yaml
Type: String
Parameter Sets: S1
Aliases: 

Required: True
Position: 2
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="77603-121">-WebApp</span><span class="sxs-lookup"><span data-stu-id="77603-121">-WebApp</span></span>
<span data-ttu-id="77603-122">WebApp-objekt</span><span class="sxs-lookup"><span data-stu-id="77603-122">WebApp Object</span></span>

```yaml
Type: Site
Parameter Sets: S2
Aliases: 

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="77603-123">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="77603-123">CommonParameters</span></span>
<span data-ttu-id="77603-124">Den här cmdleten har stöd för de gemensamma parametrarna:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-disvariable,-utbuffer,-PipelineVariable,-verbose,-WarningAction och-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="77603-124">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="77603-125">Mer information finns i about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="77603-125">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="77603-126">KOSTNADS</span><span class="sxs-lookup"><span data-stu-id="77603-126">INPUTS</span></span>

### <span data-ttu-id="77603-127">Webbplatsmallar</span><span class="sxs-lookup"><span data-stu-id="77603-127">Site</span></span>
<span data-ttu-id="77603-128">Parametern ' WebApp ' godkänner värdet av typen ' site ' från pipeline</span><span class="sxs-lookup"><span data-stu-id="77603-128">Parameter 'WebApp' accepts value of type 'Site' from the pipeline</span></span>

## <span data-ttu-id="77603-129">VÄRDEN</span><span class="sxs-lookup"><span data-stu-id="77603-129">OUTPUTS</span></span>

## <span data-ttu-id="77603-130">ANMÄRKNINGAR</span><span class="sxs-lookup"><span data-stu-id="77603-130">NOTES</span></span>

## <span data-ttu-id="77603-131">RELATERADE LÄNKAR</span><span class="sxs-lookup"><span data-stu-id="77603-131">RELATED LINKS</span></span>

