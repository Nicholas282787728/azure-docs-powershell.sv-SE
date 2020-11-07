---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Websites.dll-Help.xml
Module Name: Az.WebSites
ms.assetid: 100A5980-31E2-41F9-84D4-2F5F0CB78B8A
online version: https://docs.microsoft.com/en-us/powershell/module/Az.websites/get-Azwebappslot
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/Azs-tzl/src/Websites/Websites/help/Get-AzWebAppSlot.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/Azs-tzl/src/Websites/Websites/help/Get-AzWebAppSlot.md
ms.openlocfilehash: 033b0bd4458f20153ec1e9c876f12c7e7c368c0a
ms.sourcegitcommit: 4c61442a2df1cee633ce93cad9f6bc793803baa2
ms.translationtype: MT
ms.contentlocale: sv-SE
ms.lasthandoff: 04/16/2020
ms.locfileid: "93923341"
---
# <span data-ttu-id="523c2-101">Get-AzWebAppSlot</span><span class="sxs-lookup"><span data-stu-id="523c2-101">Get-AzWebAppSlot</span></span>

## <span data-ttu-id="523c2-102">Sammanfattning</span><span class="sxs-lookup"><span data-stu-id="523c2-102">SYNOPSIS</span></span>
<span data-ttu-id="523c2-103">Hämtar en Azure Web App-plats.</span><span class="sxs-lookup"><span data-stu-id="523c2-103">Gets an Azure Web App slot.</span></span>

## <span data-ttu-id="523c2-104">FRÅGESYNTAXEN</span><span class="sxs-lookup"><span data-stu-id="523c2-104">SYNTAX</span></span>

### <span data-ttu-id="523c2-105">S</span><span class="sxs-lookup"><span data-stu-id="523c2-105">S1</span></span>
```
Get-AzWebAppSlot [-ResourceGroupName] <String> [-Name] <String> [[-Slot] <String>]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="523c2-106">S2</span><span class="sxs-lookup"><span data-stu-id="523c2-106">S2</span></span>
```
Get-AzWebAppSlot [[-Slot] <String>] [-WebApp] <Site> [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

## <span data-ttu-id="523c2-107">PROBLEMBESKRIVNING</span><span class="sxs-lookup"><span data-stu-id="523c2-107">DESCRIPTION</span></span>
<span data-ttu-id="523c2-108">Cmdleten **Get-AzWebAppSlot** hämtar information om en Azure Web App-plats.</span><span class="sxs-lookup"><span data-stu-id="523c2-108">The **Get-AzWebAppSlot** cmdlet gets information about an Azure Web App Slot.</span></span>

## <span data-ttu-id="523c2-109">BESKRIVS</span><span class="sxs-lookup"><span data-stu-id="523c2-109">EXAMPLES</span></span>

### <span data-ttu-id="523c2-110">Exempel 1</span><span class="sxs-lookup"><span data-stu-id="523c2-110">Example 1</span></span>
```
PS C:\> Get-AzWebAppSlot -ResourceGroupName "Default-Web-WestUS" -Name "WebAppStandard" -Slot "Slot001"
```

<span data-ttu-id="523c2-111">Med det här kommandot får du den plats som heter Slot001 från webb programmet som heter WebAppStandard som tillhör resurs gruppens standard-väst.</span><span class="sxs-lookup"><span data-stu-id="523c2-111">This command gets the slot named Slot001 from the Web App named WebAppStandard that belongs to the resource group Default-Web-WestUS.</span></span>

## <span data-ttu-id="523c2-112">MALLPARAMETRAR</span><span class="sxs-lookup"><span data-stu-id="523c2-112">PARAMETERS</span></span>

### <span data-ttu-id="523c2-113">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="523c2-113">-DefaultProfile</span></span>
<span data-ttu-id="523c2-114">Autentiseringsuppgifter, konto, klient organisation och abonnemang som används för kommunikation med Azure.</span><span class="sxs-lookup"><span data-stu-id="523c2-114">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

```yaml
Type: IAzureContextContainer
Parameter Sets: (All)
Aliases: AzContext, AzureCredential

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="523c2-115">-Namn</span><span class="sxs-lookup"><span data-stu-id="523c2-115">-Name</span></span>
<span data-ttu-id="523c2-116">WebApp-namn</span><span class="sxs-lookup"><span data-stu-id="523c2-116">WebApp Name</span></span>

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

### <span data-ttu-id="523c2-117">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="523c2-117">-ResourceGroupName</span></span>
<span data-ttu-id="523c2-118">Resurs grupps namn</span><span class="sxs-lookup"><span data-stu-id="523c2-118">Resource Group Name</span></span>

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

### <span data-ttu-id="523c2-119">-Plats</span><span class="sxs-lookup"><span data-stu-id="523c2-119">-Slot</span></span>
<span data-ttu-id="523c2-120">WebApp-slot</span><span class="sxs-lookup"><span data-stu-id="523c2-120">WebApp Slot Name</span></span>

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

### <span data-ttu-id="523c2-121">-WebApp</span><span class="sxs-lookup"><span data-stu-id="523c2-121">-WebApp</span></span>
<span data-ttu-id="523c2-122">WebApp-objekt</span><span class="sxs-lookup"><span data-stu-id="523c2-122">WebApp Object</span></span>

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

### <span data-ttu-id="523c2-123">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="523c2-123">CommonParameters</span></span>
<span data-ttu-id="523c2-124">Den här cmdleten har stöd för de gemensamma parametrarna:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-disvariable,-utbuffer,-PipelineVariable,-verbose,-WarningAction och-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="523c2-124">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="523c2-125">Mer information finns i about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="523c2-125">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="523c2-126">KOSTNADS</span><span class="sxs-lookup"><span data-stu-id="523c2-126">INPUTS</span></span>

### <span data-ttu-id="523c2-127">Webbplatsmallar</span><span class="sxs-lookup"><span data-stu-id="523c2-127">Site</span></span>
<span data-ttu-id="523c2-128">Parametern ' WebApp ' godkänner värdet av typen ' site ' från pipeline</span><span class="sxs-lookup"><span data-stu-id="523c2-128">Parameter 'WebApp' accepts value of type 'Site' from the pipeline</span></span>

## <span data-ttu-id="523c2-129">VÄRDEN</span><span class="sxs-lookup"><span data-stu-id="523c2-129">OUTPUTS</span></span>

## <span data-ttu-id="523c2-130">ANMÄRKNINGAR</span><span class="sxs-lookup"><span data-stu-id="523c2-130">NOTES</span></span>

## <span data-ttu-id="523c2-131">RELATERADE LÄNKAR</span><span class="sxs-lookup"><span data-stu-id="523c2-131">RELATED LINKS</span></span>

[<span data-ttu-id="523c2-132">New-AzWebAppSlot</span><span class="sxs-lookup"><span data-stu-id="523c2-132">New-AzWebAppSlot</span></span>](./New-AzWebAppSlot.md)

[<span data-ttu-id="523c2-133">Remove-AzWebAppSlot</span><span class="sxs-lookup"><span data-stu-id="523c2-133">Remove-AzWebAppSlot</span></span>](./Remove-AzWebAppSlot.md)

[<span data-ttu-id="523c2-134">Restart-AzWebAppSlot</span><span class="sxs-lookup"><span data-stu-id="523c2-134">Restart-AzWebAppSlot</span></span>](./Restart-AzWebAppSlot.md)

[<span data-ttu-id="523c2-135">Set-AzWebAppSlot</span><span class="sxs-lookup"><span data-stu-id="523c2-135">Set-AzWebAppSlot</span></span>](./Set-AzWebAppSlot.md)

[<span data-ttu-id="523c2-136">Start-AzWebAppSlot</span><span class="sxs-lookup"><span data-stu-id="523c2-136">Start-AzWebAppSlot</span></span>](./Start-AzWebAppSlot.md)

[<span data-ttu-id="523c2-137">Stopp-AzWebAppSlot</span><span class="sxs-lookup"><span data-stu-id="523c2-137">Stop-AzWebAppSlot</span></span>](./Stop-AzWebAppSlot.md)

[<span data-ttu-id="523c2-138">Get-AzWebApp</span><span class="sxs-lookup"><span data-stu-id="523c2-138">Get-AzWebApp</span></span>](./Get-AzWebApp.md)
