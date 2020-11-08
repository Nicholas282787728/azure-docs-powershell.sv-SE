---
external help file: Microsoft.WindowsAzure.Commands.StorSimple.dll-Help.xml
ms.assetid: A1E143A8-70F2-4158-9A10-F2082AD62A73
online version: ''
schema: 2.0.0
ms.openlocfilehash: 371291f4bd33809bc2f5880e4380c448219ed37a
ms.sourcegitcommit: 56ed085a868afa8263f8eb0f755b5822f5c29532
ms.translationtype: MT
ms.contentlocale: sv-SE
ms.lasthandoff: 07/18/2020
ms.locfileid: "94099242"
---
# <span data-ttu-id="785ed-101">Stop-AzureStorSimpleJob</span><span class="sxs-lookup"><span data-stu-id="785ed-101">Stop-AzureStorSimpleJob</span></span>

## <span data-ttu-id="785ed-102">Sammanfattning</span><span class="sxs-lookup"><span data-stu-id="785ed-102">SYNOPSIS</span></span>
<span data-ttu-id="785ed-103">Stoppar ett StorSimple jobb.</span><span class="sxs-lookup"><span data-stu-id="785ed-103">Stops a StorSimple job.</span></span>

## <span data-ttu-id="785ed-104">FRÅGESYNTAXEN</span><span class="sxs-lookup"><span data-stu-id="785ed-104">SYNTAX</span></span>

```
Stop-AzureStorSimpleJob -InstanceId <String> [-Force] [-Profile <AzureSMProfile>] [<CommonParameters>]
```

## <span data-ttu-id="785ed-105">PROBLEMBESKRIVNING</span><span class="sxs-lookup"><span data-stu-id="785ed-105">DESCRIPTION</span></span>
<span data-ttu-id="785ed-106">Cmdleten **Stop-AzureStorSimpleJob** stoppar ett pågående StorSimple-jobb.</span><span class="sxs-lookup"><span data-stu-id="785ed-106">The **Stop-AzureStorSimpleJob** cmdlet stops an on-going StorSimple job.</span></span>
<span data-ttu-id="785ed-107">Du kan ange ett instans-ID eller ett jobbnamn.</span><span class="sxs-lookup"><span data-stu-id="785ed-107">You can specify a jobs by supplying an instance ID or a job name.</span></span>

## <span data-ttu-id="785ed-108">BESKRIVS</span><span class="sxs-lookup"><span data-stu-id="785ed-108">EXAMPLES</span></span>

### <span data-ttu-id="785ed-109">Exempel 1: stoppa jobb för en enhet</span><span class="sxs-lookup"><span data-stu-id="785ed-109">Example 1: Stop jobs for a device</span></span>
```
PS C:\>Get-AzureStorSimpleJob -DeviceName "Device07" | Stop-AzureStorSimpleJob -Force
```

<span data-ttu-id="785ed-110">Det här kommandot får jobbet för enheten som heter Device07 med hjälp av cmdleten **Get-AzureStorSimpleJob** .</span><span class="sxs-lookup"><span data-stu-id="785ed-110">This command gets the jobs for the device named Device07, by using the **Get-AzureStorSimpleJob** cmdlet.</span></span>
<span data-ttu-id="785ed-111">Kommandot skickar jobben till den aktuella cmdleten med hjälp av pipeline-operatorn.</span><span class="sxs-lookup"><span data-stu-id="785ed-111">The command passes the jobs to the current cmdlet by using the pipeline operator.</span></span>
<span data-ttu-id="785ed-112">Den aktuella cmdleten stoppar alla jobb som kommandot skickar till det.</span><span class="sxs-lookup"><span data-stu-id="785ed-112">The current cmdlet stops any jobs that the command passes to it.</span></span>
<span data-ttu-id="785ed-113">Kommandot anger parametern *Force* och ber dig inte att få en bekräftelse innan den stoppar ett jobb.</span><span class="sxs-lookup"><span data-stu-id="785ed-113">The command specifies the *Force* parameter, and, so, it does not prompt you for confirmation before it stops a job.</span></span>

### <span data-ttu-id="785ed-114">Exempel 2: stoppa ett visst jobb</span><span class="sxs-lookup"><span data-stu-id="785ed-114">Example 2: Stop a specific job</span></span>
```
PS C:\>Stop-AzureStorSimpleJob -InstanceId "574f47e0-44e9-495c-b8a5-0203c57ebf6d" -Force
```

<span data-ttu-id="785ed-115">Det här kommandot stoppar det jobb som har angivet instans-ID.</span><span class="sxs-lookup"><span data-stu-id="785ed-115">This command stops the job that has the specified instance ID.</span></span>

## <span data-ttu-id="785ed-116">MALLPARAMETRAR</span><span class="sxs-lookup"><span data-stu-id="785ed-116">PARAMETERS</span></span>

### <span data-ttu-id="785ed-117">-Force</span><span class="sxs-lookup"><span data-stu-id="785ed-117">-Force</span></span>
<span data-ttu-id="785ed-118">Tvingar kommandot att köras utan att fråga efter bekräftelse.</span><span class="sxs-lookup"><span data-stu-id="785ed-118">Forces the command to run without asking for user confirmation.</span></span>

```yaml
Type: SwitchParameter
Parameter Sets: (All)
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="785ed-119">-InstanceId</span><span class="sxs-lookup"><span data-stu-id="785ed-119">-InstanceId</span></span>
<span data-ttu-id="785ed-120">Anger ID för det enhets jobb som ska stoppas.</span><span class="sxs-lookup"><span data-stu-id="785ed-120">Specifies the ID of the device job to stop.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="785ed-121">-Profil</span><span class="sxs-lookup"><span data-stu-id="785ed-121">-Profile</span></span>
<span data-ttu-id="785ed-122">Anger en Azure-profil.</span><span class="sxs-lookup"><span data-stu-id="785ed-122">Specifies an Azure profile.</span></span>

```yaml
Type: AzureSMProfile
Parameter Sets: (All)
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="785ed-123">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="785ed-123">CommonParameters</span></span>
<span data-ttu-id="785ed-124">Den här cmdleten har stöd för de gemensamma parametrarna:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-disvariable,-utbuffer,-PipelineVariable,-verbose,-WarningAction och-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="785ed-124">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="785ed-125">Mer information finns i about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="785ed-125">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="785ed-126">KOSTNADS</span><span class="sxs-lookup"><span data-stu-id="785ed-126">INPUTS</span></span>

### <span data-ttu-id="785ed-127">Ingen</span><span class="sxs-lookup"><span data-stu-id="785ed-127">None</span></span>

## <span data-ttu-id="785ed-128">VÄRDEN</span><span class="sxs-lookup"><span data-stu-id="785ed-128">OUTPUTS</span></span>

### <span data-ttu-id="785ed-129">DeviceJobDetails</span><span class="sxs-lookup"><span data-stu-id="785ed-129">DeviceJobDetails</span></span>
<span data-ttu-id="785ed-130">Denna cmdlet hämtar information om **DeviceJob** som denna cmdlet slutar.</span><span class="sxs-lookup"><span data-stu-id="785ed-130">This cmdlet gets details of the **DeviceJob** that this cmdlet stops.</span></span>

## <span data-ttu-id="785ed-131">ANMÄRKNINGAR</span><span class="sxs-lookup"><span data-stu-id="785ed-131">NOTES</span></span>

## <span data-ttu-id="785ed-132">RELATERADE LÄNKAR</span><span class="sxs-lookup"><span data-stu-id="785ed-132">RELATED LINKS</span></span>

[<span data-ttu-id="785ed-133">Get-AzureStorSimpleJob</span><span class="sxs-lookup"><span data-stu-id="785ed-133">Get-AzureStorSimpleJob</span></span>](./Get-AzureStorSimpleJob.md)


