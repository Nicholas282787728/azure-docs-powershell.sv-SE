---
external help file: Microsoft.Azure.PowerShell.Cmdlets.IotHub.dll-Help.xml
Module Name: Az.IotHub
online version: https://docs.microsoft.com/en-us/powershell/module/az.iothub/new-aziothubimportdevice
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/Azs-tzl/src/IotHub/IotHub/help/New-AzIotHubImportDevice.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/Azs-tzl/src/IotHub/IotHub/help/New-AzIotHubImportDevice.md
ms.openlocfilehash: 50f0652f477edad13fb661683b1ee2f2f13fef9d
ms.sourcegitcommit: 4c61442a2df1cee633ce93cad9f6bc793803baa2
ms.translationtype: MT
ms.contentlocale: sv-SE
ms.lasthandoff: 04/16/2020
ms.locfileid: "93924514"
---
# <span data-ttu-id="7d3f6-101">New-AzIotHubImportDevice</span><span class="sxs-lookup"><span data-stu-id="7d3f6-101">New-AzIotHubImportDevice</span></span>

## <span data-ttu-id="7d3f6-102">Sammanfattning</span><span class="sxs-lookup"><span data-stu-id="7d3f6-102">SYNOPSIS</span></span>
<span data-ttu-id="7d3f6-103">Skapar ett nytt import utrustnings jobb.</span><span class="sxs-lookup"><span data-stu-id="7d3f6-103">Creates a new import devices job.</span></span>

## <span data-ttu-id="7d3f6-104">FRÅGESYNTAXEN</span><span class="sxs-lookup"><span data-stu-id="7d3f6-104">SYNTAX</span></span>

```
New-AzIotHubImportDevice [-ResourceGroupName] <String> [-Name] <String> [-InputBlobContainerUri] <String>
 [-OutputBlobContainerUri] <String> [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

## <span data-ttu-id="7d3f6-105">PROBLEMBESKRIVNING</span><span class="sxs-lookup"><span data-stu-id="7d3f6-105">DESCRIPTION</span></span>
<span data-ttu-id="7d3f6-106">Skapar ett nytt import enheter jobb för IotHub.</span><span class="sxs-lookup"><span data-stu-id="7d3f6-106">Creates a new import devices job for the IotHub.</span></span>
<span data-ttu-id="7d3f6-107">Detta importerar alla enheter till IotHub från den angivna behållaren.</span><span class="sxs-lookup"><span data-stu-id="7d3f6-107">This will import all the devices to the IotHub from the specified container.</span></span> <span data-ttu-id="7d3f6-108">Läs följande artikel om hur du skapar SAS URI.</span><span class="sxs-lookup"><span data-stu-id="7d3f6-108">Refer to the following article on how to generate the SAS URI.</span></span>
<span data-ttu-id="7d3f6-109"> https://docs.microsoft.com/azure/iot-hub/iot-hub-bulk-identity-mgmt#get-the-container-sas-uri .</span><span class="sxs-lookup"><span data-stu-id="7d3f6-109">https://docs.microsoft.com/azure/iot-hub/iot-hub-bulk-identity-mgmt#get-the-container-sas-uri .</span></span>

## <span data-ttu-id="7d3f6-110">BESKRIVS</span><span class="sxs-lookup"><span data-stu-id="7d3f6-110">EXAMPLES</span></span>

### <span data-ttu-id="7d3f6-111">Exempel 1</span><span class="sxs-lookup"><span data-stu-id="7d3f6-111">Example 1</span></span>
```
PS C:\> New-AzIotHubImportDevice -ResourceGroupName "myresourcegroup" -Name "myiothub" -InputBlobContainerUri "https://mystorageaccount.blob.core.windows.net/mystoragecontainer?sv=2015-04-05&ss=bfqt&sr=c&srt=sco&sp=rwdl&se=2016-10-27T04:01:48Z&st=2016-10-26T20:01:48Z&spr=https&sig=QqpIhHsIMF8hNuFO%3D" -OutputBlobContainerUri "https://mystorageaccount.blob.core.windows.net/?sv=2015-04-05&ss=bfqt&sr=c&srt=sco&sp=rwdl&se=2016-10-27T04:01:48Z&st=2016-10-26T20:01:48Z&spr=https&sig=QqpIhHsIMF8hNuFO%3D"
```

<span data-ttu-id="7d3f6-112">Skapar en ny begäran om import enhet för IotHub "myiothub".</span><span class="sxs-lookup"><span data-stu-id="7d3f6-112">Creates a new import device request for the IotHub "myiothub".</span></span>

## <span data-ttu-id="7d3f6-113">MALLPARAMETRAR</span><span class="sxs-lookup"><span data-stu-id="7d3f6-113">PARAMETERS</span></span>

### <span data-ttu-id="7d3f6-114">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="7d3f6-114">-DefaultProfile</span></span>
<span data-ttu-id="7d3f6-115">Autentiseringsuppgifter, konto, klient organisation och abonnemang som används för kommunikation med Azure</span><span class="sxs-lookup"><span data-stu-id="7d3f6-115">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="7d3f6-116">-InputBlobContainerUri</span><span class="sxs-lookup"><span data-stu-id="7d3f6-116">-InputBlobContainerUri</span></span>
<span data-ttu-id="7d3f6-117">URI för BLOB-behållare för FileUpload</span><span class="sxs-lookup"><span data-stu-id="7d3f6-117">Input Blob Container Uri for FileUpload</span></span>

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

### <span data-ttu-id="7d3f6-118">-Namn</span><span class="sxs-lookup"><span data-stu-id="7d3f6-118">-Name</span></span>
<span data-ttu-id="7d3f6-119">Namn på IotHub</span><span class="sxs-lookup"><span data-stu-id="7d3f6-119">Name of the IotHub</span></span>

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

### <span data-ttu-id="7d3f6-120">-OutputBlobContainerUri</span><span class="sxs-lookup"><span data-stu-id="7d3f6-120">-OutputBlobContainerUri</span></span>
<span data-ttu-id="7d3f6-121">Den URI som utdata ska skrivas till.</span><span class="sxs-lookup"><span data-stu-id="7d3f6-121">The Uri to write the output to.</span></span> 

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: True
Position: 3
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="7d3f6-122">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="7d3f6-122">-ResourceGroupName</span></span>
<span data-ttu-id="7d3f6-123">Resurs grupps namn</span><span class="sxs-lookup"><span data-stu-id="7d3f6-123">Resource Group Name</span></span>

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

### <span data-ttu-id="7d3f6-124">-Bekräfta</span><span class="sxs-lookup"><span data-stu-id="7d3f6-124">-Confirm</span></span>
<span data-ttu-id="7d3f6-125">Du uppmanas att bekräfta innan du kör cmdleten.</span><span class="sxs-lookup"><span data-stu-id="7d3f6-125">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="7d3f6-126">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="7d3f6-126">-WhatIf</span></span>
<span data-ttu-id="7d3f6-127">Visar vad som händer om cmdleten körs.</span><span class="sxs-lookup"><span data-stu-id="7d3f6-127">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="7d3f6-128">Cmdleten körs inte.</span><span class="sxs-lookup"><span data-stu-id="7d3f6-128">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="7d3f6-129">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="7d3f6-129">CommonParameters</span></span>
<span data-ttu-id="7d3f6-130">Den här cmdleten har stöd för de gemensamma parametrarna:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-disvariable,-utbuffer,-PipelineVariable,-verbose,-WarningAction och-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="7d3f6-130">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="7d3f6-131">Mer information finns i about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="7d3f6-131">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="7d3f6-132">KOSTNADS</span><span class="sxs-lookup"><span data-stu-id="7d3f6-132">INPUTS</span></span>

### <span data-ttu-id="7d3f6-133">System. String</span><span class="sxs-lookup"><span data-stu-id="7d3f6-133">System.String</span></span>

## <span data-ttu-id="7d3f6-134">VÄRDEN</span><span class="sxs-lookup"><span data-stu-id="7d3f6-134">OUTPUTS</span></span>

### <span data-ttu-id="7d3f6-135">Microsoft. Azure. commands. Management. IotHub. Models. PSIotHubJobResponse</span><span class="sxs-lookup"><span data-stu-id="7d3f6-135">Microsoft.Azure.Commands.Management.IotHub.Models.PSIotHubJobResponse</span></span>

## <span data-ttu-id="7d3f6-136">ANMÄRKNINGAR</span><span class="sxs-lookup"><span data-stu-id="7d3f6-136">NOTES</span></span>

## <span data-ttu-id="7d3f6-137">RELATERADE LÄNKAR</span><span class="sxs-lookup"><span data-stu-id="7d3f6-137">RELATED LINKS</span></span>
