---
external help file: Microsoft.Azure.PowerShell.Cmdlets.DataBoxEdge.dll-Help.xml
Module Name: Az.DataBoxEdge
online version: https://docs.microsoft.com/en-us/powershell/module/az.databoxedge/new-azdataboxedgeuser
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/Azs-tzl/src/DataBoxEdge/DataBoxEdge/help/New-AzDataBoxEdgeUser.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/Azs-tzl/src/DataBoxEdge/DataBoxEdge/help/New-AzDataBoxEdgeUser.md
ms.openlocfilehash: 480c0a8e932b672542595983f33fd19bab6fec3b
ms.sourcegitcommit: 4c61442a2df1cee633ce93cad9f6bc793803baa2
ms.translationtype: MT
ms.contentlocale: sv-SE
ms.lasthandoff: 04/16/2020
ms.locfileid: "93924641"
---
# <span data-ttu-id="3038c-101">New-AzDataBoxEdgeUser</span><span class="sxs-lookup"><span data-stu-id="3038c-101">New-AzDataBoxEdgeUser</span></span>

## <span data-ttu-id="3038c-102">Sammanfattning</span><span class="sxs-lookup"><span data-stu-id="3038c-102">SYNOPSIS</span></span>
<span data-ttu-id="3038c-103">Skapar en ny användare för enheten.</span><span class="sxs-lookup"><span data-stu-id="3038c-103">Creates a new user for the device.</span></span>

## <span data-ttu-id="3038c-104">FRÅGESYNTAXEN</span><span class="sxs-lookup"><span data-stu-id="3038c-104">SYNTAX</span></span>

```
New-AzDataBoxEdgeUser [-ResourceGroupName] <String> [-DeviceName] <String> [-Name] <String>
 -Password <SecureString> -EncryptionKey <SecureString> [-AsJob] [-DefaultProfile <IAzureContextContainer>]
 [[-Type] <String>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="3038c-105">PROBLEMBESKRIVNING</span><span class="sxs-lookup"><span data-stu-id="3038c-105">DESCRIPTION</span></span>
<span data-ttu-id="3038c-106">Den **nya AzDataBoxEdgeUser-** cmdleten skapar en ny användare för data Box Edge-enheten.</span><span class="sxs-lookup"><span data-stu-id="3038c-106">The **New-AzDataBoxEdgeUser** cmdlet creates a new user for the Data Box Edge device.</span></span> <span data-ttu-id="3038c-107">Det går bara att skapa en typ av användare `Share` .</span><span class="sxs-lookup"><span data-stu-id="3038c-107">Creation of only users of type `Share` is supported.</span></span>

## <span data-ttu-id="3038c-108">BESKRIVS</span><span class="sxs-lookup"><span data-stu-id="3038c-108">EXAMPLES</span></span>

### <span data-ttu-id="3038c-109">Exempel 1</span><span class="sxs-lookup"><span data-stu-id="3038c-109">Example 1</span></span>
```powershell
PS C:\> New-AzDataBoxEdgeUser -ResourceGroupName resourceGroupName -DeviceName deviceName -Name username
 -Password password-secured-string -EncryptionKey encryption-key
User name   Type  ResourceGroupName DeviceName
---------   ----  ----------------- ----------
username    Share resourceGroupName deviceName
```

```powershell
PS C:\> New-AzDataBoxEdgeUser -ResourceGroupName resourceGroupName -DeviceName deviceName -Name username
 -Password password-secured-string -EncryptionKey encryption-key -Type Share
User name   Type  ResourceGroupName DeviceName
---------   ----  ----------------- ----------
username    Share resourceGroupName deviceName
```

## <span data-ttu-id="3038c-110">MALLPARAMETRAR</span><span class="sxs-lookup"><span data-stu-id="3038c-110">PARAMETERS</span></span>

### <span data-ttu-id="3038c-111">-AsJob</span><span class="sxs-lookup"><span data-stu-id="3038c-111">-AsJob</span></span>
<span data-ttu-id="3038c-112">Kör cmdlet i bakgrunden</span><span class="sxs-lookup"><span data-stu-id="3038c-112">Run cmdlet in the background</span></span>

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

### <span data-ttu-id="3038c-113">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="3038c-113">-DefaultProfile</span></span>
<span data-ttu-id="3038c-114">Autentiseringsuppgifter, konto, klient organisation och abonnemang som används för kommunikation med Azure.</span><span class="sxs-lookup"><span data-stu-id="3038c-114">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="3038c-115">-Enhets namn</span><span class="sxs-lookup"><span data-stu-id="3038c-115">-DeviceName</span></span>
<span data-ttu-id="3038c-116">Enhetens namn</span><span class="sxs-lookup"><span data-stu-id="3038c-116">Device Name</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: True
Position: 1
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="3038c-117">-EncryptionKey</span><span class="sxs-lookup"><span data-stu-id="3038c-117">-EncryptionKey</span></span>
<span data-ttu-id="3038c-118">Enhetens krypterings nycklar</span><span class="sxs-lookup"><span data-stu-id="3038c-118">Encryption key of the Edge device</span></span>

```yaml
Type: System.Security.SecureString
Parameter Sets: (All)
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="3038c-119">-Namn</span><span class="sxs-lookup"><span data-stu-id="3038c-119">-Name</span></span>
<span data-ttu-id="3038c-120">Namnen</span><span class="sxs-lookup"><span data-stu-id="3038c-120">Username</span></span>

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

### <span data-ttu-id="3038c-121">-Lösen ord</span><span class="sxs-lookup"><span data-stu-id="3038c-121">-Password</span></span>
<span data-ttu-id="3038c-122">Lösen ord, ange som en säker sträng</span><span class="sxs-lookup"><span data-stu-id="3038c-122">Password, provide as a secure string</span></span>

```yaml
Type: System.Security.SecureString
Parameter Sets: (All)
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="3038c-123">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="3038c-123">-ResourceGroupName</span></span>
<span data-ttu-id="3038c-124">Resurs grupps namn</span><span class="sxs-lookup"><span data-stu-id="3038c-124">Resource Group Name</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: True
Position: 0
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="3038c-125">– Skriv</span><span class="sxs-lookup"><span data-stu-id="3038c-125">-Type</span></span>
<span data-ttu-id="3038c-126">Välj UserType</span><span class="sxs-lookup"><span data-stu-id="3038c-126">Select UserType</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: False
Position: 2
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="3038c-127">-Bekräfta</span><span class="sxs-lookup"><span data-stu-id="3038c-127">-Confirm</span></span>
<span data-ttu-id="3038c-128">Du uppmanas att bekräfta innan du kör cmdleten.</span><span class="sxs-lookup"><span data-stu-id="3038c-128">Prompts you for confirmation before running the cmdlet.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases: cf

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="3038c-129">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="3038c-129">-WhatIf</span></span>
<span data-ttu-id="3038c-130">Visar vad som händer om cmdleten körs.</span><span class="sxs-lookup"><span data-stu-id="3038c-130">Shows what would happen if the cmdlet runs.</span></span> <span data-ttu-id="3038c-131">Cmdleten körs inte.</span><span class="sxs-lookup"><span data-stu-id="3038c-131">The cmdlet is not run.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases: wi

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="3038c-132">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="3038c-132">CommonParameters</span></span>
<span data-ttu-id="3038c-133">Den här cmdleten har stöd för de gemensamma parametrarna:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-disvariable,-utbuffer,-PipelineVariable,-verbose,-WarningAction och-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="3038c-133">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="3038c-134">Mer information finns i [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="3038c-134">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="3038c-135">KOSTNADS</span><span class="sxs-lookup"><span data-stu-id="3038c-135">INPUTS</span></span>

### <span data-ttu-id="3038c-136">Ingen</span><span class="sxs-lookup"><span data-stu-id="3038c-136">None</span></span>

## <span data-ttu-id="3038c-137">VÄRDEN</span><span class="sxs-lookup"><span data-stu-id="3038c-137">OUTPUTS</span></span>

### <span data-ttu-id="3038c-138">Microsoft.Azure.PowerShell.Cmdlets.DataBoxEdge.Models.PSDataBoxEdgeDevice</span><span class="sxs-lookup"><span data-stu-id="3038c-138">Microsoft.Azure.PowerShell.Cmdlets.DataBoxEdge.Models.PSDataBoxEdgeDevice</span></span>

## <span data-ttu-id="3038c-139">ANMÄRKNINGAR</span><span class="sxs-lookup"><span data-stu-id="3038c-139">NOTES</span></span>

## <span data-ttu-id="3038c-140">RELATERADE LÄNKAR</span><span class="sxs-lookup"><span data-stu-id="3038c-140">RELATED LINKS</span></span>
