---
external help file: Microsoft.Azure.Commands.Websites.dll-Help.xml
Module Name: AzureRM
ms.assetid: 86E0D477-DD32-49BD-82E7-1CF191E4F612
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.websites/stop-azurermwebappslot
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Websites/Commands.Websites/help/Stop-AzureRmWebAppSlot.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Websites/Commands.Websites/help/Stop-AzureRmWebAppSlot.md
ms.openlocfilehash: 59fb1d649f5893dc09caa9799cd3412feae06deb
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: sv-SE
ms.lasthandoff: 08/20/2020
ms.locfileid: "93574113"
---
# <span data-ttu-id="f6671-101">Stop-AzureRmWebAppSlot</span><span class="sxs-lookup"><span data-stu-id="f6671-101">Stop-AzureRmWebAppSlot</span></span>

## <span data-ttu-id="f6671-102">Sammanfattning</span><span class="sxs-lookup"><span data-stu-id="f6671-102">SYNOPSIS</span></span>
<span data-ttu-id="f6671-103">Stoppar en Azure Web App-plats.</span><span class="sxs-lookup"><span data-stu-id="f6671-103">Stops an Azure Web App slot.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="f6671-104">FRÅGESYNTAXEN</span><span class="sxs-lookup"><span data-stu-id="f6671-104">SYNTAX</span></span>

### <span data-ttu-id="f6671-105">S</span><span class="sxs-lookup"><span data-stu-id="f6671-105">S1</span></span>
```
Stop-AzureRmWebAppSlot [-ResourceGroupName] <String> [-Name] <String> [-Slot] <String>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="f6671-106">S2</span><span class="sxs-lookup"><span data-stu-id="f6671-106">S2</span></span>
```
Stop-AzureRmWebAppSlot [-WebApp] <Site> [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="f6671-107">PROBLEMBESKRIVNING</span><span class="sxs-lookup"><span data-stu-id="f6671-107">DESCRIPTION</span></span>
<span data-ttu-id="f6671-108">Cmdleten **Stop-AzureRmWebAppSlot** stoppar en Azure Web App-plats.</span><span class="sxs-lookup"><span data-stu-id="f6671-108">The **Stop-AzureRmWebAppSlot** cmdlet stops an Azure Web App Slot.</span></span>

## <span data-ttu-id="f6671-109">BESKRIVS</span><span class="sxs-lookup"><span data-stu-id="f6671-109">EXAMPLES</span></span>

### <span data-ttu-id="f6671-110">Exempel 1</span><span class="sxs-lookup"><span data-stu-id="f6671-110">Example 1</span></span>
```
PS C:\>Stop-AzureRmWebAppSlot -ResourceGroupName "Default-Web-WestUS" -Name "ContosoWebApp" -Slot "Slot001"
```

<span data-ttu-id="f6671-111">Det här kommandot stoppar fack Slot001 för webb programmet som heter ContosoWebApp som tillhör resurs gruppen med namnet default-Web-West.</span><span class="sxs-lookup"><span data-stu-id="f6671-111">This command stops the slot Slot001 pertaining to the Web App named ContosoWebApp that belongs to the resource group named Default-Web-WestUS.</span></span>

## <span data-ttu-id="f6671-112">MALLPARAMETRAR</span><span class="sxs-lookup"><span data-stu-id="f6671-112">PARAMETERS</span></span>

### <span data-ttu-id="f6671-113">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="f6671-113">-DefaultProfile</span></span>
<span data-ttu-id="f6671-114">Autentiseringsuppgifter, konto, klient organisation och abonnemang som används för kommunikation med Azure.</span><span class="sxs-lookup"><span data-stu-id="f6671-114">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="f6671-115">-Namn</span><span class="sxs-lookup"><span data-stu-id="f6671-115">-Name</span></span>
<span data-ttu-id="f6671-116">WebApp-namn</span><span class="sxs-lookup"><span data-stu-id="f6671-116">WebApp Name</span></span>

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

### <span data-ttu-id="f6671-117">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="f6671-117">-ResourceGroupName</span></span>
<span data-ttu-id="f6671-118">Resurs grupps namn</span><span class="sxs-lookup"><span data-stu-id="f6671-118">Resource Group Name</span></span>

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

### <span data-ttu-id="f6671-119">-Plats</span><span class="sxs-lookup"><span data-stu-id="f6671-119">-Slot</span></span>
<span data-ttu-id="f6671-120">WebApp-slot</span><span class="sxs-lookup"><span data-stu-id="f6671-120">WebApp Slot Name</span></span>

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

### <span data-ttu-id="f6671-121">-WebApp</span><span class="sxs-lookup"><span data-stu-id="f6671-121">-WebApp</span></span>
<span data-ttu-id="f6671-122">WebApp-objekt</span><span class="sxs-lookup"><span data-stu-id="f6671-122">WebApp Object</span></span>

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

### <span data-ttu-id="f6671-123">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="f6671-123">CommonParameters</span></span>
<span data-ttu-id="f6671-124">Den här cmdleten har stöd för de gemensamma parametrarna:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-disvariable,-utbuffer,-PipelineVariable,-verbose,-WarningAction och-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="f6671-124">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="f6671-125">Mer information finns i about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="f6671-125">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="f6671-126">KOSTNADS</span><span class="sxs-lookup"><span data-stu-id="f6671-126">INPUTS</span></span>

### <span data-ttu-id="f6671-127">Webbplatsmallar</span><span class="sxs-lookup"><span data-stu-id="f6671-127">Site</span></span>
<span data-ttu-id="f6671-128">Parametern ' WebApp ' godkänner värdet av typen ' site ' från pipeline</span><span class="sxs-lookup"><span data-stu-id="f6671-128">Parameter 'WebApp' accepts value of type 'Site' from the pipeline</span></span>

## <span data-ttu-id="f6671-129">VÄRDEN</span><span class="sxs-lookup"><span data-stu-id="f6671-129">OUTPUTS</span></span>

## <span data-ttu-id="f6671-130">ANMÄRKNINGAR</span><span class="sxs-lookup"><span data-stu-id="f6671-130">NOTES</span></span>

## <span data-ttu-id="f6671-131">RELATERADE LÄNKAR</span><span class="sxs-lookup"><span data-stu-id="f6671-131">RELATED LINKS</span></span>
