---
external help file: Microsoft.Azure.Commands.Websites.dll-Help.xml
Module Name: AzureRM.WebSites
ms.assetid: 0FDDDEE1-CEAD-46DA-A7EB-EE477ED59749
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.websites/start-azurermwebappslot
schema: 2.0.0
ms.openlocfilehash: 97bf4078ca09ce250fea0d7c660629fbab651974
ms.sourcegitcommit: b9b2dea3441d1532a5564ddca3dced45424fe2d6
ms.translationtype: MT
ms.contentlocale: sv-SE
ms.lasthandoff: 08/15/2020
ms.locfileid: "93930437"
---
# <span data-ttu-id="704a8-101">Start-AzureRmWebAppSlot</span><span class="sxs-lookup"><span data-stu-id="704a8-101">Start-AzureRmWebAppSlot</span></span>

## <span data-ttu-id="704a8-102">Sammanfattning</span><span class="sxs-lookup"><span data-stu-id="704a8-102">SYNOPSIS</span></span>
<span data-ttu-id="704a8-103">Startar en Azure Web App-plats.</span><span class="sxs-lookup"><span data-stu-id="704a8-103">Starts an Azure Web App slot.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="704a8-104">FRÅGESYNTAXEN</span><span class="sxs-lookup"><span data-stu-id="704a8-104">SYNTAX</span></span>

### <span data-ttu-id="704a8-105">S</span><span class="sxs-lookup"><span data-stu-id="704a8-105">S1</span></span>
```
Start-AzureRmWebAppSlot [-ResourceGroupName] <String> [-Name] <String> [-Slot] <String>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="704a8-106">S2</span><span class="sxs-lookup"><span data-stu-id="704a8-106">S2</span></span>
```
Start-AzureRmWebAppSlot [-WebApp] <Site> [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="704a8-107">PROBLEMBESKRIVNING</span><span class="sxs-lookup"><span data-stu-id="704a8-107">DESCRIPTION</span></span>
<span data-ttu-id="704a8-108">Cmdleten **Start-AzureRmWebAppSlot** startar en Azure Web App-plats.</span><span class="sxs-lookup"><span data-stu-id="704a8-108">The **Start-AzureRmWebAppSlot** cmdlet starts an Azure Web App Slot.</span></span>

## <span data-ttu-id="704a8-109">BESKRIVS</span><span class="sxs-lookup"><span data-stu-id="704a8-109">EXAMPLES</span></span>

### <span data-ttu-id="704a8-110">Exempel 1</span><span class="sxs-lookup"><span data-stu-id="704a8-110">Example 1</span></span>
```
PS C:\>Start-AzureRmWebAppSlot -ResourceGroupName "Default-Web-WestUS" -Name "ContosoWebApp" -Slot "Slot001"
```

<span data-ttu-id="704a8-111">Det här kommandot startar facket som heter Slot001 som hör till webb programmet som heter ContosoWebApp och som tillhör resurs gruppen som heter default-West-väst.</span><span class="sxs-lookup"><span data-stu-id="704a8-111">This command starts the Slot named Slot001 pertaining to the Web App named ContosoWebApp that belongs to the resource group named Default-Web-WestUS.</span></span>

## <span data-ttu-id="704a8-112">MALLPARAMETRAR</span><span class="sxs-lookup"><span data-stu-id="704a8-112">PARAMETERS</span></span>

### <span data-ttu-id="704a8-113">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="704a8-113">-DefaultProfile</span></span>
<span data-ttu-id="704a8-114">Autentiseringsuppgifter, konto, klient organisation och abonnemang som används för kommunikation med Azure.</span><span class="sxs-lookup"><span data-stu-id="704a8-114">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="704a8-115">-Namn</span><span class="sxs-lookup"><span data-stu-id="704a8-115">-Name</span></span>
<span data-ttu-id="704a8-116">WebApp-namn</span><span class="sxs-lookup"><span data-stu-id="704a8-116">WebApp Name</span></span>

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

### <span data-ttu-id="704a8-117">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="704a8-117">-ResourceGroupName</span></span>
<span data-ttu-id="704a8-118">Resurs grupps namn</span><span class="sxs-lookup"><span data-stu-id="704a8-118">Resource Group Name</span></span>

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

### <span data-ttu-id="704a8-119">-Plats</span><span class="sxs-lookup"><span data-stu-id="704a8-119">-Slot</span></span>
<span data-ttu-id="704a8-120">WebApp-slot</span><span class="sxs-lookup"><span data-stu-id="704a8-120">WebApp Slot Name</span></span>

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

### <span data-ttu-id="704a8-121">-WebApp</span><span class="sxs-lookup"><span data-stu-id="704a8-121">-WebApp</span></span>
<span data-ttu-id="704a8-122">WebApp-objekt</span><span class="sxs-lookup"><span data-stu-id="704a8-122">WebApp Object</span></span>

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

### <span data-ttu-id="704a8-123">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="704a8-123">CommonParameters</span></span>
<span data-ttu-id="704a8-124">Den här cmdleten har stöd för de gemensamma parametrarna:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-disvariable,-utbuffer,-PipelineVariable,-verbose,-WarningAction och-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="704a8-124">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="704a8-125">Mer information finns i about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="704a8-125">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="704a8-126">KOSTNADS</span><span class="sxs-lookup"><span data-stu-id="704a8-126">INPUTS</span></span>

### <span data-ttu-id="704a8-127">Webbplatsmallar</span><span class="sxs-lookup"><span data-stu-id="704a8-127">Site</span></span>
<span data-ttu-id="704a8-128">Parametern ' WebApp ' godkänner värdet av typen ' site ' från pipeline</span><span class="sxs-lookup"><span data-stu-id="704a8-128">Parameter 'WebApp' accepts value of type 'Site' from the pipeline</span></span>

## <span data-ttu-id="704a8-129">VÄRDEN</span><span class="sxs-lookup"><span data-stu-id="704a8-129">OUTPUTS</span></span>

## <span data-ttu-id="704a8-130">ANMÄRKNINGAR</span><span class="sxs-lookup"><span data-stu-id="704a8-130">NOTES</span></span>

## <span data-ttu-id="704a8-131">RELATERADE LÄNKAR</span><span class="sxs-lookup"><span data-stu-id="704a8-131">RELATED LINKS</span></span>

[<span data-ttu-id="704a8-132">Get-AzureRMWebAppSlot</span><span class="sxs-lookup"><span data-stu-id="704a8-132">Get-AzureRMWebAppSlot</span></span>](./Get-AzureRMWebAppSlot.md)

[<span data-ttu-id="704a8-133">New-AzureRMWebAppSlot</span><span class="sxs-lookup"><span data-stu-id="704a8-133">New-AzureRMWebAppSlot</span></span>](./New-AzureRMWebAppSlot.md)

[<span data-ttu-id="704a8-134">Remove-AzureRMWebAppSlot</span><span class="sxs-lookup"><span data-stu-id="704a8-134">Remove-AzureRMWebAppSlot</span></span>](./Remove-AzureRMWebAppSlot.md)

[<span data-ttu-id="704a8-135">Restart-AzureRMWebAppSlot</span><span class="sxs-lookup"><span data-stu-id="704a8-135">Restart-AzureRMWebAppSlot</span></span>](./Restart-AzureRMWebAppSlot.md)

[<span data-ttu-id="704a8-136">Set-AzureRMWebAppSlot</span><span class="sxs-lookup"><span data-stu-id="704a8-136">Set-AzureRMWebAppSlot</span></span>](./Set-AzureRMWebAppSlot.md)

[<span data-ttu-id="704a8-137">Stopp-AzureRMWebAppSlot</span><span class="sxs-lookup"><span data-stu-id="704a8-137">Stop-AzureRMWebAppSlot</span></span>](./Stop-AzureRMWebAppSlot.md)

[<span data-ttu-id="704a8-138">Get-AzureRmWebApp</span><span class="sxs-lookup"><span data-stu-id="704a8-138">Get-AzureRmWebApp</span></span>](./Get-AzureRmWebApp.md)
