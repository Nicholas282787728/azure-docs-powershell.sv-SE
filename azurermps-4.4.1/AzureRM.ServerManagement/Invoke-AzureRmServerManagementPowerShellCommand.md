---
external help file: Microsoft.Azure.Commands.ServerManagement.dll-Help.xml
Module Name: AzureRM.ServerManagement
ms.assetid: 1EA5F348-5EF4-4056-BA06-7B95E12E329D
online version: ''
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/ServerManagement/Commands.ServerManagement/help/Invoke-AzureRmServerManagementPowerShellCommand.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/ServerManagement/Commands.ServerManagement/help/Invoke-AzureRmServerManagementPowerShellCommand.md
ms.openlocfilehash: 5acd510118f2be26ba09f3e0fefbc9b0c80aae02
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: sv-SE
ms.lasthandoff: 08/20/2020
ms.locfileid: "93577467"
---
# <span data-ttu-id="0be4d-101">Invoke-AzureRmServerManagementPowerShellCommand</span><span class="sxs-lookup"><span data-stu-id="0be4d-101">Invoke-AzureRmServerManagementPowerShellCommand</span></span>

## <span data-ttu-id="0be4d-102">Sammanfattning</span><span class="sxs-lookup"><span data-stu-id="0be4d-102">SYNOPSIS</span></span>
<span data-ttu-id="0be4d-103">Kör ett skript block för Windows PowerShell på en nod.</span><span class="sxs-lookup"><span data-stu-id="0be4d-103">Executes a Windows PowerShell script block on a node.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="0be4d-104">FRÅGESYNTAXEN</span><span class="sxs-lookup"><span data-stu-id="0be4d-104">SYNTAX</span></span>

### <span data-ttu-id="0be4d-105">ByName</span><span class="sxs-lookup"><span data-stu-id="0be4d-105">ByName</span></span>
```
Invoke-AzureRmServerManagementPowerShellCommand [-ResourceGroupName] <String> [-NodeName] <String>
 [-SessionName] <String> [-Command] <ScriptBlock> [-PowerShellSessionName <String>] [-RawOutput]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="0be4d-106">BySession</span><span class="sxs-lookup"><span data-stu-id="0be4d-106">BySession</span></span>
```
Invoke-AzureRmServerManagementPowerShellCommand [-Session] <Session> [-Command] <ScriptBlock>
 [-PowerShellSessionName <String>] [-RawOutput] [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="0be4d-107">PROBLEMBESKRIVNING</span><span class="sxs-lookup"><span data-stu-id="0be4d-107">DESCRIPTION</span></span>
<span data-ttu-id="0be4d-108">Cmdleten **Invoke-AzureRmServerManagementPowerShellCommand** kör ett skript block för Windows PowerShell på en nod som hanteras av en Azure Server Management Gateway.</span><span class="sxs-lookup"><span data-stu-id="0be4d-108">The **Invoke-AzureRmServerManagementPowerShellCommand** cmdlet executes a Windows PowerShell script block on a node managed by an Azure Server Management Gateway.</span></span>

## <span data-ttu-id="0be4d-109">BESKRIVS</span><span class="sxs-lookup"><span data-stu-id="0be4d-109">EXAMPLES</span></span>

## <span data-ttu-id="0be4d-110">MALLPARAMETRAR</span><span class="sxs-lookup"><span data-stu-id="0be4d-110">PARAMETERS</span></span>

### <span data-ttu-id="0be4d-111">-Kommando</span><span class="sxs-lookup"><span data-stu-id="0be4d-111">-Command</span></span>
<span data-ttu-id="0be4d-112">Anger det skript block som ska köras på målnoden.</span><span class="sxs-lookup"><span data-stu-id="0be4d-112">Specifies the script block to run on the target node.</span></span>

```yaml
Type: System.Management.Automation.ScriptBlock
Parameter Sets: (All)
Aliases: 

Required: True
Position: 3
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="0be4d-113">-Nodnamn</span><span class="sxs-lookup"><span data-stu-id="0be4d-113">-NodeName</span></span>
<span data-ttu-id="0be4d-114">Anger namnet på den nod som skript blocket ska köras på.</span><span class="sxs-lookup"><span data-stu-id="0be4d-114">Specifies the name of the node to run the script block on.</span></span>

```yaml
Type: System.String
Parameter Sets: ByName
Aliases: 

Required: True
Position: 1
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="0be4d-115">-PowerShellSessionName</span><span class="sxs-lookup"><span data-stu-id="0be4d-115">-PowerShellSessionName</span></span>
<span data-ttu-id="0be4d-116">Anger namnet på Windows PowerShell-startsidan på målnoden.</span><span class="sxs-lookup"><span data-stu-id="0be4d-116">Specifies the name of the Windows PowerShell run space on the target node.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="0be4d-117">-RawOutput</span><span class="sxs-lookup"><span data-stu-id="0be4d-117">-RawOutput</span></span>
<span data-ttu-id="0be4d-118">Anger att cmdleten returnerar det fullständiga objekt som innehåller utdata från noden.</span><span class="sxs-lookup"><span data-stu-id="0be4d-118">Indicates that the cmdlet returns the complete object that contains the output from the node.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="0be4d-119">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="0be4d-119">-ResourceGroupName</span></span>
<span data-ttu-id="0be4d-120">Anger namnet på den resurs grupp som noden tillhör.</span><span class="sxs-lookup"><span data-stu-id="0be4d-120">Specifies the name of the resource group that the node belongs to.</span></span>

```yaml
Type: System.String
Parameter Sets: ByName
Aliases: 

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="0be4d-121">-Session</span><span class="sxs-lookup"><span data-stu-id="0be4d-121">-Session</span></span>
<span data-ttu-id="0be4d-122">Anger det **session** -objekt som denna cmdlet använder för att ansluta till målnoden.</span><span class="sxs-lookup"><span data-stu-id="0be4d-122">Specifies the **Session** object that this cmdlet uses to connect to the target node.</span></span>

<span data-ttu-id="0be4d-123">Den här parametern kan anges i stället för parametrarna *ResourceGroupName* , *nodnamn* , *sessionname* och *PowerShellSessionName* .</span><span class="sxs-lookup"><span data-stu-id="0be4d-123">This parameter may be specified instead of the *ResourceGroupName* , *NodeName* , *SessionName* , and *PowerShellSessionName* parameters.</span></span>

```yaml
Type: Microsoft.Azure.Commands.ServerManagement.Model.Session
Parameter Sets: BySession
Aliases: 

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="0be4d-124">-Sessionsnamn</span><span class="sxs-lookup"><span data-stu-id="0be4d-124">-SessionName</span></span>
<span data-ttu-id="0be4d-125">Anger namnet på den session som ska hantera noden.</span><span class="sxs-lookup"><span data-stu-id="0be4d-125">Specifies the name of the session to manage the node.</span></span>

```yaml
Type: System.String
Parameter Sets: ByName
Aliases: 

Required: True
Position: 2
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="0be4d-126">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="0be4d-126">-DefaultProfile</span></span>
<span data-ttu-id="0be4d-127">Autentiseringsuppgifter, konto, klient organisation och abonnemang som används för kommunikation med Azure.</span><span class="sxs-lookup"><span data-stu-id="0be4d-127">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="0be4d-128">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="0be4d-128">CommonParameters</span></span>
<span data-ttu-id="0be4d-129">Den här cmdleten har stöd för de gemensamma parametrarna:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-disvariable,-utbuffer,-PipelineVariable,-verbose,-WarningAction och-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="0be4d-129">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="0be4d-130">Mer information finns i about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="0be4d-130">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="0be4d-131">KOSTNADS</span><span class="sxs-lookup"><span data-stu-id="0be4d-131">INPUTS</span></span>

### <span data-ttu-id="0be4d-132">Dialogsessionen</span><span class="sxs-lookup"><span data-stu-id="0be4d-132">Session</span></span>
<span data-ttu-id="0be4d-133">Parametern ' session ' godkänner värdet för typen session från pipeline</span><span class="sxs-lookup"><span data-stu-id="0be4d-133">Parameter 'Session' accepts value of type 'Session' from the pipeline</span></span>

## <span data-ttu-id="0be4d-134">VÄRDEN</span><span class="sxs-lookup"><span data-stu-id="0be4d-134">OUTPUTS</span></span>

### <span data-ttu-id="0be4d-135">System. Object</span><span class="sxs-lookup"><span data-stu-id="0be4d-135">System.Object</span></span>

## <span data-ttu-id="0be4d-136">ANMÄRKNINGAR</span><span class="sxs-lookup"><span data-stu-id="0be4d-136">NOTES</span></span>

## <span data-ttu-id="0be4d-137">RELATERADE LÄNKAR</span><span class="sxs-lookup"><span data-stu-id="0be4d-137">RELATED LINKS</span></span>

[<span data-ttu-id="0be4d-138">Azure Server Management-cmdletar</span><span class="sxs-lookup"><span data-stu-id="0be4d-138">Azure Server Management Cmdlets</span></span>](./AzureRM.ServerManagement.md)


