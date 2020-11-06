---
external help file: Microsoft.Azure.Commands.IotHub.dll-Help.xml
Module Name: AzureRM.IotHub
online version: ''
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/IotHub/Commands.IotHub/help/New-AzureRmIotHubExportDevices.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/IotHub/Commands.IotHub/help/New-AzureRmIotHubExportDevices.md
ms.openlocfilehash: 3191f4e451ec010a3918130142d08da6f08b3990
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: sv-SE
ms.lasthandoff: 08/20/2020
ms.locfileid: "93584716"
---
# <span data-ttu-id="0d030-101">New-AzureRmIotHubExportDevices</span><span class="sxs-lookup"><span data-stu-id="0d030-101">New-AzureRmIotHubExportDevices</span></span>

## <span data-ttu-id="0d030-102">Sammanfattning</span><span class="sxs-lookup"><span data-stu-id="0d030-102">SYNOPSIS</span></span>
<span data-ttu-id="0d030-103">Skapar ett nytt export enheter jobb.</span><span class="sxs-lookup"><span data-stu-id="0d030-103">Creates a new export devices job.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="0d030-104">FRÅGESYNTAXEN</span><span class="sxs-lookup"><span data-stu-id="0d030-104">SYNTAX</span></span>

```
New-AzureRmIotHubExportDevices [-ResourceGroupName] <String> [-Name] <String>
 [-ExportBlobContainerUri] <String> [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

## <span data-ttu-id="0d030-105">PROBLEMBESKRIVNING</span><span class="sxs-lookup"><span data-stu-id="0d030-105">DESCRIPTION</span></span>
<span data-ttu-id="0d030-106">Skapar ett nytt export enheter jobb för IotHub.</span><span class="sxs-lookup"><span data-stu-id="0d030-106">Creates a new export devices job for the IotHub.</span></span>
<span data-ttu-id="0d030-107">Då exporteras alla enheter till den angivna behållaren.</span><span class="sxs-lookup"><span data-stu-id="0d030-107">This will export all the devices to the specified container.</span></span> <span data-ttu-id="0d030-108">Läs följande artikel om hur du skapar SAS URI.</span><span class="sxs-lookup"><span data-stu-id="0d030-108">Refer to the following article on how to generate the SAS URI.</span></span>
<span data-ttu-id="0d030-109"> https://azure.microsoft.com/en-us/documentation/articles/iot-hub-bulk-identity-mgmt/ .</span><span class="sxs-lookup"><span data-stu-id="0d030-109">https://azure.microsoft.com/en-us/documentation/articles/iot-hub-bulk-identity-mgmt/ .</span></span>

## <span data-ttu-id="0d030-110">BESKRIVS</span><span class="sxs-lookup"><span data-stu-id="0d030-110">EXAMPLES</span></span>

### <span data-ttu-id="0d030-111">Exempel 1 skickar en begäran om export enhet.</span><span class="sxs-lookup"><span data-stu-id="0d030-111">Example 1 Issue an export device request.</span></span>
```
PS C:\> New-AzureRmIotHubExportDevices -ResourceGroupName "myresourcegroup" -Name "myiothub" -ExportBlobContainerUri "https://mystorageaccount.blob.core.windows.net/?sv=2015-04-05&ss=bfqt&sr=c&srt=sco&sp=rwdl&se=2016-10-27T04:01:48Z&st=2016-10-26T20:01:48Z&spr=https&sig=QqpIhHsIMF8hNuFO%3D" -ExcludeKeys $true
```

<span data-ttu-id="0d030-112">Skapar en ny begäran om export enhet för IotHub "myiothub" Förutom nycklarna.</span><span class="sxs-lookup"><span data-stu-id="0d030-112">Creates a new export device request for the IotHub "myiothub" excluding the keys.</span></span>

## <span data-ttu-id="0d030-113">MALLPARAMETRAR</span><span class="sxs-lookup"><span data-stu-id="0d030-113">PARAMETERS</span></span>

### <span data-ttu-id="0d030-114">-ExportBlobContainerUri</span><span class="sxs-lookup"><span data-stu-id="0d030-114">-ExportBlobContainerUri</span></span>
<span data-ttu-id="0d030-115">URI som du vill exportera blobben till.</span><span class="sxs-lookup"><span data-stu-id="0d030-115">The Uri to export the blob to.</span></span> 

```yaml
Type: System.String
Parameter Sets: (All)
Aliases: 

Required: True
Position: 2
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="0d030-116">-Namn</span><span class="sxs-lookup"><span data-stu-id="0d030-116">-Name</span></span>
<span data-ttu-id="0d030-117">Namn på IotHub</span><span class="sxs-lookup"><span data-stu-id="0d030-117">Name of the IotHub</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases: 

Required: True
Position: 1
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="0d030-118">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="0d030-118">-ResourceGroupName</span></span>
<span data-ttu-id="0d030-119">Resurs grupps namn</span><span class="sxs-lookup"><span data-stu-id="0d030-119">Resource Group Name</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases: 

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="0d030-120">-Bekräfta</span><span class="sxs-lookup"><span data-stu-id="0d030-120">-Confirm</span></span>
<span data-ttu-id="0d030-121">Du uppmanas att bekräfta innan du kör cmdleten.</span><span class="sxs-lookup"><span data-stu-id="0d030-121">Prompts you for confirmation before running the cmdlet.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases: cf

Required: False
Position: Named
Default value: False
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="0d030-122">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="0d030-122">-WhatIf</span></span>
<span data-ttu-id="0d030-123">Visar vad som händer om cmdleten körs.</span><span class="sxs-lookup"><span data-stu-id="0d030-123">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="0d030-124">Cmdleten körs inte.</span><span class="sxs-lookup"><span data-stu-id="0d030-124">The cmdlet is not run.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases: wi

Required: False
Position: Named
Default value: False
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="0d030-125">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="0d030-125">-DefaultProfile</span></span>
<span data-ttu-id="0d030-126">Autentiseringsuppgifter, konto, klient organisation och abonnemang som används för kommunikation med Azure.</span><span class="sxs-lookup"><span data-stu-id="0d030-126">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

```yaml
Type: Microsoft.Azure.Commands.Common.Authentication.Abstractions.IAzureContextContainer
Parameter Sets: (All)
Aliases: AzureRmContext, AzureCredential

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="0d030-127">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="0d030-127">CommonParameters</span></span>
<span data-ttu-id="0d030-128">Den här cmdleten har stöd för de gemensamma parametrarna:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-disvariable,-utbuffer,-PipelineVariable,-verbose,-WarningAction och-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="0d030-128">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="0d030-129">Mer information finns i about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="0d030-129">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="0d030-130">KOSTNADS</span><span class="sxs-lookup"><span data-stu-id="0d030-130">INPUTS</span></span>

### <span data-ttu-id="0d030-131">System. String</span><span class="sxs-lookup"><span data-stu-id="0d030-131">System.String</span></span>

## <span data-ttu-id="0d030-132">VÄRDEN</span><span class="sxs-lookup"><span data-stu-id="0d030-132">OUTPUTS</span></span>

### <span data-ttu-id="0d030-133">Microsoft. Azure. Management. IotHub. Models. JobResponse</span><span class="sxs-lookup"><span data-stu-id="0d030-133">Microsoft.Azure.Management.IotHub.Models.JobResponse</span></span>

## <span data-ttu-id="0d030-134">ANMÄRKNINGAR</span><span class="sxs-lookup"><span data-stu-id="0d030-134">NOTES</span></span>

## <span data-ttu-id="0d030-135">RELATERADE LÄNKAR</span><span class="sxs-lookup"><span data-stu-id="0d030-135">RELATED LINKS</span></span>

