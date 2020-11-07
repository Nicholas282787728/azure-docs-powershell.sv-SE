---
external help file: Microsoft.Azure.Commands.IotHub.dll-Help.xml
Module Name: AzureRM.IotHub
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.iothub/new-azurermiothubexportdevices
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/IotHub/Commands.IotHub/help/New-AzureRmIotHubExportDevices.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/IotHub/Commands.IotHub/help/New-AzureRmIotHubExportDevices.md
ms.openlocfilehash: 2f9122b2683721aa7f92bc1695b6c314e83d76c4
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: sv-SE
ms.lasthandoff: 08/20/2020
ms.locfileid: "93757681"
---
# <span data-ttu-id="6c0ae-101">New-AzureRmIotHubExportDevices</span><span class="sxs-lookup"><span data-stu-id="6c0ae-101">New-AzureRmIotHubExportDevices</span></span>

## <span data-ttu-id="6c0ae-102">Sammanfattning</span><span class="sxs-lookup"><span data-stu-id="6c0ae-102">SYNOPSIS</span></span>
<span data-ttu-id="6c0ae-103">Skapar ett nytt export enheter jobb.</span><span class="sxs-lookup"><span data-stu-id="6c0ae-103">Creates a new export devices job.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="6c0ae-104">FRÅGESYNTAXEN</span><span class="sxs-lookup"><span data-stu-id="6c0ae-104">SYNTAX</span></span>

```
New-AzureRmIotHubExportDevices [-ResourceGroupName] <String> [-Name] <String>
 [-ExportBlobContainerUri] <String> [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

## <span data-ttu-id="6c0ae-105">PROBLEMBESKRIVNING</span><span class="sxs-lookup"><span data-stu-id="6c0ae-105">DESCRIPTION</span></span>
<span data-ttu-id="6c0ae-106">Skapar ett nytt export enheter jobb för IotHub.</span><span class="sxs-lookup"><span data-stu-id="6c0ae-106">Creates a new export devices job for the IotHub.</span></span>
<span data-ttu-id="6c0ae-107">Då exporteras alla enheter till den angivna behållaren.</span><span class="sxs-lookup"><span data-stu-id="6c0ae-107">This will export all the devices to the specified container.</span></span> <span data-ttu-id="6c0ae-108">Läs följande artikel om hur du skapar SAS URI.</span><span class="sxs-lookup"><span data-stu-id="6c0ae-108">Refer to the following article on how to generate the SAS URI.</span></span>
<span data-ttu-id="6c0ae-109"> https://azure.microsoft.com/en-us/documentation/articles/iot-hub-bulk-identity-mgmt/ .</span><span class="sxs-lookup"><span data-stu-id="6c0ae-109">https://azure.microsoft.com/en-us/documentation/articles/iot-hub-bulk-identity-mgmt/ .</span></span>

## <span data-ttu-id="6c0ae-110">BESKRIVS</span><span class="sxs-lookup"><span data-stu-id="6c0ae-110">EXAMPLES</span></span>

### <span data-ttu-id="6c0ae-111">Exempel 1 skickar en begäran om export enhet.</span><span class="sxs-lookup"><span data-stu-id="6c0ae-111">Example 1 Issue an export device request.</span></span>
```
PS C:\> New-AzureRmIotHubExportDevices -ResourceGroupName "myresourcegroup" -Name "myiothub" -ExportBlobContainerUri "https://mystorageaccount.blob.core.windows.net/?sv=2015-04-05&ss=bfqt&sr=c&srt=sco&sp=rwdl&se=2016-10-27T04:01:48Z&st=2016-10-26T20:01:48Z&spr=https&sig=QqpIhHsIMF8hNuFO%3D" -ExcludeKeys $true
```

<span data-ttu-id="6c0ae-112">Skapar en ny begäran om export enhet för IotHub "myiothub" Förutom nycklarna.</span><span class="sxs-lookup"><span data-stu-id="6c0ae-112">Creates a new export device request for the IotHub "myiothub" excluding the keys.</span></span>

## <span data-ttu-id="6c0ae-113">MALLPARAMETRAR</span><span class="sxs-lookup"><span data-stu-id="6c0ae-113">PARAMETERS</span></span>

### <span data-ttu-id="6c0ae-114">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="6c0ae-114">-DefaultProfile</span></span>
<span data-ttu-id="6c0ae-115">Autentiseringsuppgifter, konto, klient organisation och abonnemang som används för kommunikation med Azure</span><span class="sxs-lookup"><span data-stu-id="6c0ae-115">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="6c0ae-116">-ExportBlobContainerUri</span><span class="sxs-lookup"><span data-stu-id="6c0ae-116">-ExportBlobContainerUri</span></span>
<span data-ttu-id="6c0ae-117">URI som du vill exportera blobben till.</span><span class="sxs-lookup"><span data-stu-id="6c0ae-117">The Uri to export the blob to.</span></span> 

```yaml
Type: String
Parameter Sets: (All)
Aliases: 

Required: True
Position: 2
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="6c0ae-118">-Namn</span><span class="sxs-lookup"><span data-stu-id="6c0ae-118">-Name</span></span>
<span data-ttu-id="6c0ae-119">Namn på IotHub</span><span class="sxs-lookup"><span data-stu-id="6c0ae-119">Name of the IotHub</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: 

Required: True
Position: 1
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="6c0ae-120">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="6c0ae-120">-ResourceGroupName</span></span>
<span data-ttu-id="6c0ae-121">Resurs grupps namn</span><span class="sxs-lookup"><span data-stu-id="6c0ae-121">Resource Group Name</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: 

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="6c0ae-122">-Bekräfta</span><span class="sxs-lookup"><span data-stu-id="6c0ae-122">-Confirm</span></span>
<span data-ttu-id="6c0ae-123">Du uppmanas att bekräfta innan du kör cmdleten.</span><span class="sxs-lookup"><span data-stu-id="6c0ae-123">Prompts you for confirmation before running the cmdlet.</span></span>

```yaml
Type: SwitchParameter
Parameter Sets: (All)
Aliases: cf

Required: False
Position: Named
Default value: False
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="6c0ae-124">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="6c0ae-124">-WhatIf</span></span>
<span data-ttu-id="6c0ae-125">Visar vad som händer om cmdleten körs.</span><span class="sxs-lookup"><span data-stu-id="6c0ae-125">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="6c0ae-126">Cmdleten körs inte.</span><span class="sxs-lookup"><span data-stu-id="6c0ae-126">The cmdlet is not run.</span></span>

```yaml
Type: SwitchParameter
Parameter Sets: (All)
Aliases: wi

Required: False
Position: Named
Default value: False
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="6c0ae-127">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="6c0ae-127">CommonParameters</span></span>
<span data-ttu-id="6c0ae-128">Den här cmdleten har stöd för de gemensamma parametrarna:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-disvariable,-utbuffer,-PipelineVariable,-verbose,-WarningAction och-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="6c0ae-128">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="6c0ae-129">Mer information finns i about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="6c0ae-129">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="6c0ae-130">KOSTNADS</span><span class="sxs-lookup"><span data-stu-id="6c0ae-130">INPUTS</span></span>

### <span data-ttu-id="6c0ae-131">System. String</span><span class="sxs-lookup"><span data-stu-id="6c0ae-131">System.String</span></span>

## <span data-ttu-id="6c0ae-132">VÄRDEN</span><span class="sxs-lookup"><span data-stu-id="6c0ae-132">OUTPUTS</span></span>

### <span data-ttu-id="6c0ae-133">Microsoft. Azure. Management. IotHub. Models. JobResponse</span><span class="sxs-lookup"><span data-stu-id="6c0ae-133">Microsoft.Azure.Management.IotHub.Models.JobResponse</span></span>

## <span data-ttu-id="6c0ae-134">ANMÄRKNINGAR</span><span class="sxs-lookup"><span data-stu-id="6c0ae-134">NOTES</span></span>

## <span data-ttu-id="6c0ae-135">RELATERADE LÄNKAR</span><span class="sxs-lookup"><span data-stu-id="6c0ae-135">RELATED LINKS</span></span>

