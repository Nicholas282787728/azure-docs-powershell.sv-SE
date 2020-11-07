---
external help file: Microsoft.Azure.Commands.Websites.dll-Help.xml
Module Name: AzureRM.WebSites
ms.assetid: 100A5980-31E2-41F9-84D4-2F5F0CB78B8A
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.websites/get-azurermwebappslot
schema: 2.0.0
ms.openlocfilehash: 9ac20046317fa7d070e69284696293e1f66ed486
ms.sourcegitcommit: b9b2dea3441d1532a5564ddca3dced45424fe2d6
ms.translationtype: MT
ms.contentlocale: sv-SE
ms.lasthandoff: 08/15/2020
ms.locfileid: "93929182"
---
# <span data-ttu-id="5a90d-101">Get-AzureRmWebAppSlot</span><span class="sxs-lookup"><span data-stu-id="5a90d-101">Get-AzureRmWebAppSlot</span></span>

## <span data-ttu-id="5a90d-102">Sammanfattning</span><span class="sxs-lookup"><span data-stu-id="5a90d-102">SYNOPSIS</span></span>
<span data-ttu-id="5a90d-103">Hämtar en Azure Web App-plats.</span><span class="sxs-lookup"><span data-stu-id="5a90d-103">Gets an Azure Web App slot.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="5a90d-104">FRÅGESYNTAXEN</span><span class="sxs-lookup"><span data-stu-id="5a90d-104">SYNTAX</span></span>

### <span data-ttu-id="5a90d-105">S</span><span class="sxs-lookup"><span data-stu-id="5a90d-105">S1</span></span>
```
Get-AzureRmWebAppSlot [-ResourceGroupName] <String> [-Name] <String> [[-Slot] <String>]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="5a90d-106">S2</span><span class="sxs-lookup"><span data-stu-id="5a90d-106">S2</span></span>
```
Get-AzureRmWebAppSlot [[-Slot] <String>] [-WebApp] <Site> [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

## <span data-ttu-id="5a90d-107">PROBLEMBESKRIVNING</span><span class="sxs-lookup"><span data-stu-id="5a90d-107">DESCRIPTION</span></span>
<span data-ttu-id="5a90d-108">Cmdleten **Get-AzureRmWebAppSlot** hämtar information om en Azure Web App-plats.</span><span class="sxs-lookup"><span data-stu-id="5a90d-108">The **Get-AzureRmWebAppSlot** cmdlet gets information about an Azure Web App Slot.</span></span>

## <span data-ttu-id="5a90d-109">BESKRIVS</span><span class="sxs-lookup"><span data-stu-id="5a90d-109">EXAMPLES</span></span>

### <span data-ttu-id="5a90d-110">Exempel 1</span><span class="sxs-lookup"><span data-stu-id="5a90d-110">Example 1</span></span>
```
PS C:\> Get-AzureRmWebAppSlot -ResourceGroupName "Default-Web-WestUS" -Name "WebAppStandard" -Slot "Slot001"
```

<span data-ttu-id="5a90d-111">Med det här kommandot får du den plats som heter Slot001 från webb programmet som heter WebAppStandard som tillhör resurs gruppens standard-väst.</span><span class="sxs-lookup"><span data-stu-id="5a90d-111">This command gets the slot named Slot001 from the Web App named WebAppStandard that belongs to the resource group Default-Web-WestUS.</span></span>

## <span data-ttu-id="5a90d-112">MALLPARAMETRAR</span><span class="sxs-lookup"><span data-stu-id="5a90d-112">PARAMETERS</span></span>

### <span data-ttu-id="5a90d-113">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="5a90d-113">-DefaultProfile</span></span>
<span data-ttu-id="5a90d-114">Autentiseringsuppgifter, konto, klient organisation och abonnemang som används för kommunikation med Azure.</span><span class="sxs-lookup"><span data-stu-id="5a90d-114">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="5a90d-115">-Namn</span><span class="sxs-lookup"><span data-stu-id="5a90d-115">-Name</span></span>
<span data-ttu-id="5a90d-116">WebApp-namn</span><span class="sxs-lookup"><span data-stu-id="5a90d-116">WebApp Name</span></span>

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

### <span data-ttu-id="5a90d-117">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="5a90d-117">-ResourceGroupName</span></span>
<span data-ttu-id="5a90d-118">Resurs grupps namn</span><span class="sxs-lookup"><span data-stu-id="5a90d-118">Resource Group Name</span></span>

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

### <span data-ttu-id="5a90d-119">-Plats</span><span class="sxs-lookup"><span data-stu-id="5a90d-119">-Slot</span></span>
<span data-ttu-id="5a90d-120">WebApp-slot</span><span class="sxs-lookup"><span data-stu-id="5a90d-120">WebApp Slot Name</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: 

Required: False
Position: 2
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="5a90d-121">-WebApp</span><span class="sxs-lookup"><span data-stu-id="5a90d-121">-WebApp</span></span>
<span data-ttu-id="5a90d-122">WebApp-objekt</span><span class="sxs-lookup"><span data-stu-id="5a90d-122">WebApp Object</span></span>

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

### <span data-ttu-id="5a90d-123">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="5a90d-123">CommonParameters</span></span>
<span data-ttu-id="5a90d-124">Den här cmdleten har stöd för de gemensamma parametrarna:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-disvariable,-utbuffer,-PipelineVariable,-verbose,-WarningAction och-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="5a90d-124">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="5a90d-125">Mer information finns i about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="5a90d-125">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="5a90d-126">KOSTNADS</span><span class="sxs-lookup"><span data-stu-id="5a90d-126">INPUTS</span></span>

### <span data-ttu-id="5a90d-127">Webbplatsmallar</span><span class="sxs-lookup"><span data-stu-id="5a90d-127">Site</span></span>
<span data-ttu-id="5a90d-128">Parametern ' WebApp ' godkänner värdet av typen ' site ' från pipeline</span><span class="sxs-lookup"><span data-stu-id="5a90d-128">Parameter 'WebApp' accepts value of type 'Site' from the pipeline</span></span>

## <span data-ttu-id="5a90d-129">VÄRDEN</span><span class="sxs-lookup"><span data-stu-id="5a90d-129">OUTPUTS</span></span>

## <span data-ttu-id="5a90d-130">ANMÄRKNINGAR</span><span class="sxs-lookup"><span data-stu-id="5a90d-130">NOTES</span></span>

## <span data-ttu-id="5a90d-131">RELATERADE LÄNKAR</span><span class="sxs-lookup"><span data-stu-id="5a90d-131">RELATED LINKS</span></span>

[<span data-ttu-id="5a90d-132">New-AzureRMWebAppSlot</span><span class="sxs-lookup"><span data-stu-id="5a90d-132">New-AzureRMWebAppSlot</span></span>](./New-AzureRMWebAppSlot.md)

[<span data-ttu-id="5a90d-133">Remove-AzureRMWebAppSlot</span><span class="sxs-lookup"><span data-stu-id="5a90d-133">Remove-AzureRMWebAppSlot</span></span>](./Remove-AzureRMWebAppSlot.md)

[<span data-ttu-id="5a90d-134">Restart-AzureRMWebAppSlot</span><span class="sxs-lookup"><span data-stu-id="5a90d-134">Restart-AzureRMWebAppSlot</span></span>](./Restart-AzureRMWebAppSlot.md)

[<span data-ttu-id="5a90d-135">Set-AzureRMWebAppSlot</span><span class="sxs-lookup"><span data-stu-id="5a90d-135">Set-AzureRMWebAppSlot</span></span>](./Set-AzureRMWebAppSlot.md)

[<span data-ttu-id="5a90d-136">Start-AzureRMWebAppSlot</span><span class="sxs-lookup"><span data-stu-id="5a90d-136">Start-AzureRMWebAppSlot</span></span>](./Start-AzureRMWebAppSlot.md)

[<span data-ttu-id="5a90d-137">Stopp-AzureRMWebAppSlot</span><span class="sxs-lookup"><span data-stu-id="5a90d-137">Stop-AzureRMWebAppSlot</span></span>](./Stop-AzureRMWebAppSlot.md)

[<span data-ttu-id="5a90d-138">Get-AzureRmWebApp</span><span class="sxs-lookup"><span data-stu-id="5a90d-138">Get-AzureRmWebApp</span></span>](./Get-AzureRmWebApp.md)
